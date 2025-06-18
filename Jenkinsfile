pipeline {
    agent any

    tools { 
        msbuild 'MSBuild-v6'
    }

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }
        
        stage('Build app') {
            steps {
                 bat 'dotnet build'
            }
        }


        stage('Run Tests') {
            steps {
                 bat 'dotnet test'
            }
        }
    }
}
