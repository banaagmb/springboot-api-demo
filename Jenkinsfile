@Library('shared-library-a') _
pipeline {
  agent any
 
  tools {
    maven 'mvn-version'
  }
 
  stages {
    stage('Build') {
      steps {
        mavenPackage()
      }
    }

        stage("Build image") {
            steps {
                script {
                    step.buildNum()
                    step.buildImage()
                }
            }
        }
 
      stage("Push image") {
        steps {
                script {
                    step.pushImage()
                    }
               }
          }
     }
 }
