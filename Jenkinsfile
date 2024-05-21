pipeline {
  agent {
        dockerfile {
            dir '.'
            filename 'Dockerfile'
            label 'ssh'
            args '-v /var/run/docker.sock:/var/run/docker.sock -u root'
        }
    }
    stages{
        stage('checkout'){
            steps{
                checkout poll: false, scm: scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Aishwarya2991/demo-app']])
            }    
            }
        }
    }
