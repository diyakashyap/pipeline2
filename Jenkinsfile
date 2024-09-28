pipeline
{
    agent any
    stages
    {
        stage('test')
        {
            steps{withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_home', maven: 'Maven_home', mavenSettingsConfig: '', traceability: true)} {
                sh 'mvn clean test'
}
        }
        stage('Deploy')
        {
            sshagent(['DEVCICD']) {
                sh 'scp -o StrictHostKeyChecking=no webapp/target/webapps.war ec2-user@18.185.118.206:/usr/share/tomcat/webapps'
        }
        }
        
    }
}