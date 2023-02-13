pipeline {
    
    agent any
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
    }
    
    
    tools {
        maven 'maven-3.9.0'
    }
    stages {
          stage('docker pipeline'){
            steps {
                echo "Hello ${params.PERSON}"
            }
         }
        stage('git repo clone') {
            steps {
                git 'https://github.com/hanumantharao19/docker-pipeline-mhr.git'
            }
        }
        
        stage ('maven build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('build docker image') {
            steps {
                sh 'docker build -t hanumantharao1986/jan23_java:v2 .'
            }
        }
        
        stage('docker login') {
            steps {
               withCredentials([string(credentialsId: 'dokcer_pass_id', variable: 'docker_pass')]) {
                   sh 'docker login -u hanumantharao1986 -p ${docker_pass}'
                  }
            }
        }
        
        stage('docker image push to docker hub') {
            steps {
                sh 'docker push hanumantharao1986/jan23_java:v2'
            }
        }
    }
    
}
