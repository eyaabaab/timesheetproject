pipeline {
    agent any

    stages {
        stage('Git') {
            steps {
                git branch : 'master ',
                url : 'https://github.com/eyaabaab/timesheetproject.git'
            }
        }
         stage('Compile') {
            steps {
                sh 'mvn clean compile'
            }
        }
     stage('MVN Sonarqube') {
            steps {
                sh 'mvn sonar:sonar -Dsonar.login=admin -Dsonar.password=Boujmal2602* -Dmaven.test.skip=true'
            }
        }
        
    }
}
                
