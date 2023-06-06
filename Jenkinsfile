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

    stage('Install dependencies') {
      steps {
        // Install Node.js dependencies
        nodejs('NodeJS 14') {
          sh 'npm ci'
        }
      }
    }

    stage('Build') {
      steps {
        // Build the React project
        nodejs('NodeJS 14') {
          sh 'npm run build'
        }
      }
    }

    stage('Publish') {
      steps {
        // Publish the build artifacts (e.g., to a web server)
        // Modify this step according to your deployment requirements
        // For example, you can use an FTP or SCP plugin to upload the build artifacts.
        sh 'echo "Publishing the build artifacts..."'
      }
    }
  }
}
