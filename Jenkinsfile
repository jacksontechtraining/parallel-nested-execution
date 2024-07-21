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

        stage('Nested parallel Stage'){
            failFast true
            parallel{
                // stage A1
                stage('Nested parallel execution A1'){
                    stages{
                            stage('nested stage A1'){
                                steps{
                                    echo "Nested parallel execution"
                                }
                            }
                            stage('nested stage A2'){
                                steps{
                                    echo "Nested parallel execution"
                                }
                            }
                            stage('nested stage A3'){
                                steps{
                                    echo "Nested parallel execution"
                                }
                            }
                    }                    
                }

                // stage B1
                stage('Nested parallel execution B1'){
                    stages{
                            stage('nested stage B1'){
                                steps{
                                    echo "Nested parallel execution"
                                }
                            }
                            stage('nested stage B2'){
                                steps{
                                    echo "Nested parallel execution"
                                }
                            }
                            stage('nested stage B3'){
                                steps{
                                    echo "Nested parallel execution"
                                }
                            }
                    }                    
                }
            }
        }
    }
}