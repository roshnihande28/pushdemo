pipeline {
       agent any
       stages  {
        stage ('compile stage'){
            steps {
                withMaven(maven : 'maven_3_8_5'){
                    sh 'mvn clean compile'
                }
            }
        }
        
        stage ("test"){
            steps {
                withMaven(maven : 'maven_3_8_5'){
                    sh 'mvn clean test'
            }
        }
        stage ("deploy"){
            steps {
                withMaven(maven : 'maven_3_8_5'){
                    sh 'mvn deploy'
            }
        }
       }
}
