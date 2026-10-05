node {
    stage('Preparation') {
        catchError(buildResult: 'SUCCESS') {
            sh 'docker compose down -v || true'
        }
    }
      stage('Checkout') {
        checkout scm
    }
    stage('Build') {
        sh 'cd dotnet-demo-app/'
        sh 'docker compose up -d --build'
    }
}
