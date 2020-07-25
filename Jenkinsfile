pipeline{
    agent{label 'vslave1'}
    tools{
        maven 'M3'
    }
    stages{
        stage('Checkout'){
            steps{
                git 'https://github.com/vivra-git/spring-petclinic.git'
            }
        }
        stage('Build'){
            steps{
                 sh 'mvn clean compile'
            }
        }
        stage('Test'){
            steps{
                    sh 'mvn clean compile'
                    // sh 'mvn test'
                     // junit '**/target/surefire-reports/TEST-*.xml'
            }
        }
        stage('Package'){
            steps{
                // sh 'mvn package'
                //archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
                sh 'mvn clean compile'
                }
        }
        stage('Reports'){
            steps{
                sh 'mvn clean compile'
                #publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: 'target/site/jacoco', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: ''])     
                }
        }   
    }
}

