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
def mvnHome = tool name: 'maven', type: 'maven'
sh "${mvnHome}/bin/mvn -version"
}
}
}
}

