pipeline {
         agent any
         stages {
                
stage('unit Test'){
steps {
sh 'ant -f test.xml'
}
}
stage('build') {
                 steps {
                   sh 'ant -f build.xml'
}}
}
post {
 always {
      archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
}
}}

