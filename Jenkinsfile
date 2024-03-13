pipeline {
  agent any
  environment {
    JAVA_HOME = '/usr/lib/jvm/java-17-openjdk' // Specify the path to your Java 17 installation
  }
  stages {
    stage ('Build') {
      steps {
        echo 'Running build automation'
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
