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
sh 'mvn -B -ntp -Dmaven.test.failure.ignore verify'
}
}
}
}

