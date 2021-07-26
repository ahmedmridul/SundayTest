pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
                bat "rmdir  /s /q cucumberwithTestNG"
                bat "git clone https://github.com/Saha58datsajib/cucumberwithTestNG.git"
                bat "mvn clean -f cucumberwithTestNG"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f cucumberwithTestNG"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f cucumberwithTestNG"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f cucumberwithTestNG"
            }
        }
    }
}
