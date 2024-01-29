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
                        git url: 'https://github.com/Josmerlym/ParaleloPipline.git'
                        bat 'npm install'
                        bat 'npm update'                       
                        bat 'npx cypress run cypress run --record --key 498c7108-34aa-40ad-8654-1b019a7317d8  --parallel'
                    
                    }
                }

                stage('Slave 2') {
                    agent {
                        label "Agente2_2"
                    }
                    steps {
                        git url: 'https://github.com/Josmerlym/ParaleloPipline.git'
                        bat 'npm install'
                        bat 'npm update'                       
                        bat 'npx cypress run cypress run --record --key 498c7108-34aa-40ad-8654-1b019a7317d8  --parallel'
                    
                    }
                }

                stage('Slave 3') {
                    agent {
                        label "Agente2_3"
                    }
                    steps {
                        git url: 'https://github.com/Josmerlym/ParaleloPipline.git'
                        bat 'npm install'
                        bat 'npm update'                       
                        bat 'npx cypress run cypress run --record --key 498c7108-34aa-40ad-8654-1b019a7317d8  --parallel'
                    
                    }
                }     

                
   
                  
            }

             
        }

    }
            
}