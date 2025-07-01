pipeline {
    agent any
    tools {
        maven 'maven'
    }
    stages {
        stage("pull the src"){
            steps {
                git branch: 'main',url: 'https://github.com/VikasGowdaHR/canara.git'
            }
        }
        stage("maven clean"){
            steps{
                sh 'mvn clean'
            }
        }
        stage("prepare the build"){
            steps{
                sh 'mvn package'
            }
        }
    }
}
