```groovy
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Sreyash-Pattnaik/DevOps.git'
            }
        }

        stage('Build') {
            steps {
                bat 'javac HelloWorld.java'
            }
        }

        stage('Run') {
            steps {
                bat 'java HelloWorld'
            }
        }

        stage('Package') {
            steps {
                bat 'jar cfe HelloWorld.jar HelloWorld HelloWorld.class'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'HelloWorld.jar',
                    fingerprint: true
            }
        }
    }
}
```
