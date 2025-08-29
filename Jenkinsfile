node {
    stage('Download') {
      git branch: 'dev', url: 'https://github.com/clouddevopseng/25code.git'
     }
     stage('Build') {
     sh 'mvn package'
     }
     stage('Deployment') {
     deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: '81aaa725-47e3-4424-a1cb-08b01041f738', path: '', url: 'http://172.31.33.159:8080')], contextPath: '/app-development', war: '**/*.war'
     }
