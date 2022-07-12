pipeline {
       agent any
       stages  {
        stage ('compile stage'){
            steps {
                withMaven(maven : 'maven_3_1_0'){
                    sh 'mvn clean compile'
                }
            }
        }
        
        stage ("test"){
            steps {
                withMaven(maven : 'maven_3_1_0'){
                    sh 'mvn clean test'
            }
        }
        stage ("deploy"){
            steps {
                withMaven(maven : 'maven_3_1_0'){
                    sh 'mvn deploy'
            }
        }
       }
}
