pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                retry(3){
                    //error("Build failed because of this and that..")
                    script{                    
                        int b=1
                        int c="${BUILD_NUMBER}"                  
                        echo "${c+b}"                   
                   }
                }                    
            }
        }
            stage('if condetion'){
                
                steps{
                    
                    echo "hello"
                }
                post {
                    always {
                        echo 'One way or another, I have finished'
                       
                    }
                    success {
                        echo 'I succeeded!'
                    }
                    unstable {
                        echo 'I am unstable :/'
                    }
                    failure {
                        echo 'I failed :('
                    }
                    changed {
                        echo 'Things were different before...'
                    }
                }
            
        }
    }
}
