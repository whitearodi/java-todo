pipeline {
    agent any
    tools{
        gradle 'gradle'
    }
    stages{
        stage('clone-repository') {
         steps { 
             git branch:'master', url:'https://github.com/whitearodi/java-todo.git'
            }
        }
        
        stage('build-code') {
            steps{
                sh 'gradle build'
            }
        }
        
        stage('test-code') {
            steps{
                sh 'gradle test'
            }
        }
    }
}