pipeline{
    agent any
       
    stages{
        stage("Restore dependencies"){
            steps{
                bat 'dotnet restore'
            } 
        }
         stage("Build  the Project"){
            steps{
                bat 'dotnet build --no-restore'
            } 
        }
        stage("Running integration and unit tests"){
            steps{
                bat 'dotnet test --no-build --verbosity normal'
            } 
        }
    }
    
}