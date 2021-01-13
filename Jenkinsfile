pipeline {
    agent any
    
    stages {
        stage ('checkout GIT SCM') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/master']],
                    url:'https://github.com/ukundoor/hello-world.git'
                    ])
            } 
        }
        stage ('build'){
            steps{
                sh 'mvn clean install package'
            }
        }
            
    }
}