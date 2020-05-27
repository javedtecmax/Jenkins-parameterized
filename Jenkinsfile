pipeline {
           agent any
           stages {
                stage("Hello") {
                     steps {
                          echo 'Hello World'
                     }
                }
                stage("jenkins") {
                     steps {
                          sh 'ls'
                      }
                }
                stage("parameterized"){
                    steps {
                        build job: 'attach-paramaterized', parameters: [[$class: 'StringParameterValue', name: 'jenkins_variable', value: "add this parameter"]]
                    }
                }
           }
}