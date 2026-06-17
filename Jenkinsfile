pipeline{
    agent any

    tools{
    mvn 'maven'
    }

    stages{
    stage('checkout'){
        steps{
    git branch:'master', url 'https://github.com/YashwanthK18/MyMavrenGuavaApp'
        }
    }
        stage('build'){
        steps{
            sh 'mvn clean package'
        }
        }
        stage('test'){
        steps{
            sh 'mvn test'
        }
        }
        stage('deploy'){
        steps{
            sh 'mvn exec:java -Dexec.mainClass="com.example.App"'
        }
        }
        
    }
    post{
        success{
            echo 'success'
        }
        failure{
            echo 'failure'
        }
    }
}
