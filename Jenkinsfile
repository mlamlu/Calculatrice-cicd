
pipeline { 
agent any
        stages {
            stage('Hello') {
                 steps {
                    echo 'Hello World'
                 }
              }
            stage('Build') { 
                steps { 
                    sh 'mvn clean compile'
                }
            }
/*             stage('test') {
                steps {
                    sh 'mvn test'
                }
            } */


            stage('package') {
                steps {
                    sh 'mvn package'
                }
            }
            stage('Deploy') { 
                steps {         
                        archiveArtifacts 'target/*.jar'
                }
            }
    }


/*     post {
            always {
                       junit '**//* surefire-reports *//*.xml'
                    }
         } */
}
