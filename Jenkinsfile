pipeline {
    agent any

    tools {nodejs "node"}

    stages {

        stage('Cypress Parallel Test Suite') {
            parallel {
                stage('Slave 1') {
                    agent {
                        label "Agente2_1"
                    }
                    steps {
                        git url: 'https://github.com/jonromerotester/Paralelo_pipline.git'
                        bat 'npm install'
                        bat 'npm update'                       
                        bat 'npx cypress run cypress run --record --key aa4c7b9e-604e-46e1-9c11-dfc06d43f8db  --parallel'
                    
                    }
                }

                
               stage('Slave 2') {
                    agent {
                        label "Agente2_2"
                    }
                    steps {
                        git url: 'https://github.com/jonromerotester/Paralelo_pipline.git'
                        bat 'npm install'
                        bat 'npm update'                       
                        bat 'npx cypress run cypress run --record --key aa4c7b9e-604e-46e1-9c11-dfc06d43f8db  --parallel'
                    
                    }
                }

                stage('Slave 3') {
                    agent {
                        label "Agente2_3"
                    }
                    steps {
                        git url: 'https://github.com/jonromerotester/Paralelo_pipline.git'
                        bat 'npm install'
                        bat 'npm update'                       
                        bat 'npx cypress run cypress run --record --key aa4c7b9e-604e-46e1-9c11-dfc06d43f8db  --parallel'
                    
                    }
                }
   
                  
            }

             
        }

    }
            
}