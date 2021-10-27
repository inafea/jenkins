pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                retry(3){
                    //error("Build failed because of this and that..")
                    script{
                    
                    int b=3
                    int c="${BUILD_NUMBER}"                  
                    echo "${c+b}"
                   
                   }
                }
                    
            }
        }
    }
}
