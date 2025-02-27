pipeline {
    agent any

    stages {
        stage('Git') {
            steps {
                git branch : 'master ',
                url : 'https://github.com/hwafa/timesheetproject.git'
            }
        }
         stage('Compile') {
            steps {
                sh 'mvn clean compile'
            }
        }
     stage('MVN Sonarqube') {
            steps {
                sh 'mvn sonar:sonar -Dsonar.login=squ_3aa266e36e53995843672eea3d576a69f9fd4eb1 -Dmaven.test.skip=true'
            }
        }
        
    }
}
                
