pipeline {
    agent any
    environment {
        PROJECT_NAME = "FirstAppWithJenkins"
        PROJECT_URL = "https://github.com/OrxanMusayev/FirstAppWithJenkins.git"
        DOTNET ="dotnet-path"
        COVERLET_OUTPUT_PATH = "coverlet-output-path"
        SONAR_SCANNER ="sonar-scanner-path"
        SONARQUBE_HOST_URL = "http://localhost:9000"
        SONARQUBE_TOKEN = "sonarqube-token"
        PROJECT_FILE_PATH ="WebApp/WebApp.csproj"
        TEST_PROJECT_FILE_PATH="WebApp.Tests/WebApp.Tests.csproj"
    }
    stages {
        
        stage('Build') {
            steps {
                echo 'Building..'
                git(
                    credentialsId:"Github",
                    url:"${PROJECT_URL}"
                )
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}