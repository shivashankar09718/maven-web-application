node {
def MavenHome = tool name: "maven3.9.4"


stage ('checkout code'){
git branch: 'development', credentialsId: '9fb9001a-1eb9-4ea6-9ad8-bb831a7e2b5b', url: 'https://github.com/shivashankar09718/maven-web-application.git'
}

stage ('build'){
sh "${MavenHome}/bin/mvn clean package"
}
/*stage ('sonar report'){
sh "${MavenHome}/bin/mvn clean sonar:sonar"
}
stage ('artifactory repo(nexus'){
sh "${MavenHome}/bin/mvn clean deploy"
}
stage ('tomcat deploy'){
sshagent(['2630b177-0142-4c69-b586-c389e008d06d']) {
sh "scp target/maven-web-application.war ec2-user@172.31.12.80:/opt/apache-tomcat-9.0.80/webapps"
}
}    
 */   
}


