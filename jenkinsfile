pipeline{
    agent any
    stages {
        stage('one'){
            steps{
                echo "hi this is my first pipeline"
            }
        }
        stage('two'){
            steps {
                input ("Do you want to procees")
            }
        }
        stage('three'){
            when {
                not {
                    branch "master"
                }
            }
            steps{
                echo "branch is not master"
            }
        }
        stage('four'){
            parallel {
                stage('unit test'){
                     steps{
                         echo "running unit testing....."
                    }
                }
                stage('integration testing'){
                        steps{
                            echo "running  the integration testing...."
                        }
                    }
                }
            }

        
        
    }
}
