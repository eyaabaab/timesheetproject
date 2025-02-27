pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/eyaabaab/timesheetproject.git', branch: 'master'
            }
        }
        stage('MVN SONARQUBE') {
            steps {
                sh 'mvn sonar:sonar -Dsonar.host.url=http://localhost:9000 -Dsonar.login=admin -Dsonar.password=Boujmal2602@'
            }
        }
    }
}
