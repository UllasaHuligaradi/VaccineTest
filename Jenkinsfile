pipeline {
    agent any

    stages {
        stage('Git Pull') {
            steps {
                script{
                     
                    bat "git checkout main"
					bat "git pull origin main"
					
					}

                }
             }
        
        stage('Run SoapUI') {
            steps {
                script{
                   bat "'C:\\Program Files\\SmartBear\\SoapUI-5.6.0\\bin\\testrunner.bat' -sVaccineTest -cCheckVaccine 'Vaccine-readyapi-project.xml' "


                }
            }
        }
        stage('Git Push Report') {
            steps {
                script{
                   bat "gitrun.sh"


                }
            }
        }
    }
}
