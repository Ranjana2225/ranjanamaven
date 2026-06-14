pipeline{
   agent any
  tools{
    maven 'Maven'
     }
    stages{
        stage('Checkout'){
            steps{
                 git branch:'master',
                   url:'https://github.com/Ranjana2225/ranjanamaven.git'
            }
        }
      stage('Build'){
        steps{
         sh 'mvn clean package'
        }
      }
      stage('Test'){
        steps{
         sh 'mvn test'
        }
      }
      stage('Run application'){
        steps{
          sh 'java -jar target/ranjanamaven-1.0-SNAPSHOT.jar'
        }
      }
    }
  post{
    success{
      echo 'Build sucessful'
    }
    failure{
      echo 'Build failed'
    }
  }
}
      

                       
