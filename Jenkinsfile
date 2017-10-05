pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build(propagate: true, job: 'VSTestRunner', wait: true)
        powershell 'scripts\\HelloWaterWorld.ps1'
      }
    }
    stage('Deploy') {
      steps {
        powershell 'scripts\\TurnToStone.ps1'
      }
    }
  }
}