pipeline {
  agent any
  options { timestamps() }
  stages {
    stage('Stage 1: Build') { steps { echo 'Task: Compile & package the app. Tool: Maven.' } }
    stage('Stage 2: Unit & Integration Tests') { steps { echo 'Task: Run unit & integration tests. Tools: JUnit + REST Assured.' } }
    stage('Stage 3: Code Analysis') { steps { echo 'Task: Static code analysis. Tool: SonarQube (SonarScanner CLI).' } }
    stage('Stage 4: Security Scan') { steps { echo 'Task: Dependency vulnerability scan. Tool: OWASP Dependency-Check.' } }
    stage('Stage 5: Deploy to Staging') { steps { echo 'Task: Deploy to staging EC2. Tool: Ansible (SSH).' } }
    stage('Stage 6: Integration Tests on Staging') { steps { echo 'Task: Run API/E2E tests against staging. Tool: Newman (Postman CLI).' } }
    stage('Stage 7: Deploy to Production') { steps { echo 'Task: Deploy to production EC2. Tool: Ansible (SSH).' } }
  }
  post { always { echo 'End of theoretical pipeline (prints tasks & tools only).' } }
}
