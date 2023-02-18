pipeline {
agent any 
stages {
stage ("git"){
steps {
git branch: 'main', credentialsId: 'github', url: 'https://github.com/nkjohn7/nk1/'
}
}
stage ("build"){
steps {
def mvnHome = tool name: '3.6.3', type: 'maven'
sh "${mvnHome}/bin/mvn -version"
}
}
}
}

