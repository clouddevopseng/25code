node {
    stage('Download') {
      git branch: 'test', url: 'https://github.com/clouddevopseng/25code.git'
     }
     stage('Build') {
     sh 'mvn package'
     }
     stage('Deployment') {
     deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: '5e1a3fd9-f193-48f9-884d-cde857455ea4', path: '', url: 'http://172.31.35.215:8080')], contextPath: '/test-app', war: '**/*.war'
     }
