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
}    
