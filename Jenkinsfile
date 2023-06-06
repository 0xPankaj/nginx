pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        // Clean workspace and checkout the repository
        cleanWs()
        checkout scm
      }
    }

    stage('Build') {
      steps {
        // Build the project
        sh 'npm install'
        sh 'npm run build'
      }
    }

    stage('Test') {
      steps {
        // Run tests
        sh 'npm run test'
      }
    }

    stage('Publish') {
      steps {
        // Publish the build artifacts or deploy to a server
        // Modify this step according to your deployment requirements
        // For example, you can use an FTP or SCP plugin to upload the build artifacts.
        sh 'echo "Publishing the build artifacts..."'
      }
    }
  }
}
