node{
    stage('Git Clone'){
        git 'https://github.com/anudeepbadam123/calcwebapp.git'
    }
    stage('Maven Package'){
        def mvnHome = tool name: 'maven-dir', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deployment'){ 
        sh 'cp target/*.war /opt/tomcat/webapps'
    }    
}
