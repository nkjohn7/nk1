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
sh "/usr/share/maven/mvn --version"
}
}
}
}

