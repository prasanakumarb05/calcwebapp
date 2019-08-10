node{
    stage('git clone'){
        git 'https://github.com/prasanakumarb05/calcwebapp.git'
    }
    stage('build'){
        def mvnHome = tool name: 'Maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deploy to Tomcat'){ 
        sh 'cp target/*.war /opt/tomcat9/webapps'
    }    
}
