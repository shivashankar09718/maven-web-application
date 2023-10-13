node {
def MavenHome = tool name: "maven3.9.4"
properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '5', artifactNumToKeepStr: '5', daysToKeepStr: '3', numToKeepStr: '5')), [$class: 'JobLocalConfiguration', changeReasonComment: ''],
            pipelineTriggers([githubPush()])])

stage ('checkout code'){
git branch: 'development', credentialsId: '9fb9001a-1eb9-4ea6-9ad8-bb831a7e2b5b', url: 'https://github.com/shivashankar09718/maven-web-application.git'
}

stage ('build'){
sh "${MavenHome}/bin/mvn clean package"
}

}


