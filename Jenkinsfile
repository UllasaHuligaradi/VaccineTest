pipeline {
    agent any

    stages {
        stage('Git Pull') {
            steps {
                script{
                     
                    sh "git checkout main"
					
					}

                }
             }
        
        stage('Run SoapUI') {
            steps {
                script{
                   sh "'C:/Program Files/SmartBear/SoapUI-5.6.0/bin/testrunner.bat' -sVaccineTest -cCheckVaccine 'Vaccine-readyapi-project.xml' "


                }
            }
        }
        stage('Git Push Report') {
            steps {
                script{
                   sh "gitrun.sh"


                }
            }
        }
    }
}
