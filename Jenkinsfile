node {
  stage('SCM') {
    git 'https://github.com/4ll3n/dotnet.git'
  }
  stage('SonarQube analysis') {
    withSonarQubeEnv('Sonar Scanner') {
      sh 'mvn clean package sonar:sonar'
    } // SonarQube taskId is automatically attached to the pipeline context
  }
}
