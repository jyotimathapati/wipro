pipeline{
    agent any
    tools{
        maven 'maven'
    }
    stages{
        stage('src pull'){
            steps{
                git branch: 'main', url: 'https://github.com/jyotimathapati/wipro.git'
            }
        }
        stage('Build stage'){
            steps{
                sh 'mvn clean package'
            }
        }
    }
    post{
        success{
            echo "success build"
        }
        failure{
            echo "failure build"
        }
    }
}
