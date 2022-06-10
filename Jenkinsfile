node {  
    def maven-home = tool name: 'mvn-home', type: 'maven' 
    stage('Git-Checkout') { 
        git branch: 'main', credentialsId: 'git-cred', url: 'https://github.com/Emmachizoba/web-app.git' 
    }
    stage('Clean-Compile') { 
        sh "${maven-home}/bin/mvn clean compile" 
    }
    stage('Package') { 
        sh "${maven-home}/bin/mvn package"
    }
}
