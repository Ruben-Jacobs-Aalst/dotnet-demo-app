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
        sh 'docker compose up -d --build'
    }
}
