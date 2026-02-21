pipeline{
    agent any
    stages{
        stage("Restore Dependencies"){
            when{
                branch "main"
            }
            steps{
                sh "dotnet restore"
            }
        }
        stage("Build Solution"){
            when{
                branch "main"
            }
            steps{
                sh "dotnet build --no-restore"
            }
        }
        stage("Run Tests"){
            when{
                branch "main"
            }
            steps{
                sh "dotnet test --no-build --verbosity normal"
            }
        }
    }
}