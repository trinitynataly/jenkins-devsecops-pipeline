pipeline {
  agent any
  options {
    timestamps()
    disableConcurrentBuilds()
  }

  stages {
    stage('Stage 1: Build') {
      steps {
        echo 'Task: Compile and package the application.'
        echo 'Tool: Maven.'
      }
    }

    stage('Stage 2: Unit and Integration Tests') {
      steps {
        echo 'Task: Run unit and integration tests.'
        echo 'Tools: JUnit (unit) and REST Assured (integration).'
      }
    }

    stage('Stage 3: Code Analysis') {
      steps {
        echo 'Task: Static code analysis to enforce standards.'
        echo 'Tool: SonarQube via SonarScanner CLI.'
      }
    }

    stage('Stage 4: Security Scan') {
      steps {
        echo 'Task: Scan source/dependencies for vulnerabilities.'
        echo 'Tool: OWASP Dependency-Check.'
      }
    }

    stage('Stage 5: Deploy to Staging') {
      steps {
        echo 'Task: Deploy artefact to a staging EC2 instance.'
        echo 'Tool: Ansible over SSH.'
      }
    }

    stage('Stage 6: Integration Tests on Staging') {
      steps {
        echo 'Task: Run API/E2E tests against staging.'
        echo 'Tool: Newman (Postman CLI).'
      }
    }

    stage('Stage 7: Deploy to Production') {
      steps {
        echo 'Task: Deploy to the production EC2 instance.'
        echo 'Tool: Ansible over SSH.'
      }
    }
  }

  post {
    always {
      echo 'End of theoretical pipeline (printing tasks & tools only).'
    }
  }
}
