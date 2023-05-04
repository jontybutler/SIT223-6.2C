pipeline{
    agent any

    stages{
        stage('Build'){
            steps{
                echo "Build the code using a build automation tool to compile and package the code."
                echo "TOOL TO BE USED - Maven"
            }
        }
        stage('Unit and Integration Tests'){
            steps{
                echo "Run unit tests to ensure the code functions as expected and run integration tests to ensure the different components of the application work together as expected."
                echo "TOOL TO BE USED - JUnit"
            }
            post{
                success{
                    mail to: "jontylbutler@gmail.com"
                    subject: "Unit and Integration tests email"
                    body: "Testing was successful!"
                    attachLog: true
                }
            }
        }
        stage('Code Analysis'){
            steps{
                echo "Use a code analysis tool to analyse the code and ensure it meets industry standards."
                echo "TOOL TO BE USED - SonarQube"
            }
        }
        stage('Security Scan'){
            steps{
                echo "Perform a security scan on the code using a tool to identify any vulnerabilities."
                echo "TOOL TO BE USED - OWASP ZAP"
            }
        }
        stage('Deploy to Staging'){
            steps{
                echo "Deploy the application to a staging server."
                echo "TOOL TO BE USED - AWS EC2 instance"
            }
        }
        stage('Integration Tests on Staging'){
            steps{
                echo "Run integration tests on the staging environment to ensure the application functions as 
                expected in a production-like environment."
                echo "TOOL TO BE USED - JUnit"
            }
        }
        stage('Deploy to Production'){
            steps{
                echo "Deploy the application to a production server."
                echo "TOOL TO BE USED - AWS EC2 instance"
            }
        }
    }
}
