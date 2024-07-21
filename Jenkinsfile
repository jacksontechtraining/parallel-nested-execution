pipeline{
    agent any
    stages{
        stage('squential execution 1'){
            steps{
                echo "non parallel execution"
            }
        }
        stage('squential execution 2'){
            steps{
                echo "non parallel execution"
            }
        }

        stage('Prallel Stage'){
            failFast true
            parallel{
                stage('parallel execution 1'){
                    steps{
                        echo "parallel execution"
                    }
                }
                stage('parallel execution 2'){
                    steps{
                        echo "parallel execution"
                    }
                }
                stage('parallel execution 3'){
                    steps{
                        echo "parallel execution"
                    }
                }
            }

        }
    }
}