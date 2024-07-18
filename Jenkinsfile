node {
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
        
        stage('Pipeline Initializations') {
            checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [[$class: 'RelativeTargetDirectory', relativeTargetDir: 'FirstAppWithJenkins']], userRemoteConfigs: [[credentialsId: 'a85ef7a0-e362-4496-a98d-768681e3a331', url: 'https://github.com/OrxanMusayev/FirstAppWithJenkins.git']]])
                    
        }
        stage('Build') {
                bat "nuget restore \"${workspace}/FirstAppWithJenkins.sln\""
           }
    }
}