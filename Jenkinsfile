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
    }
}