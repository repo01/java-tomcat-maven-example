node
{
    def mvnHome= tool name: "maven3.6.3"
    stage('Git')
    {
        git credentialsId: 'github_credentials', url: 'https://github.com/repo01/java-tomcat-maven-example.git'
    }
    stage('Build')
    {
        sh "${mvnHome}/bin/mvn clean package"
    }
    stage ("Deploy To tomcat") {
        sh "sudo cp target/*.war /var/lib/tomcat9/webapps/"
    }
}    
