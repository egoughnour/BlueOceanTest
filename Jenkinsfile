pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build(propagate: true, job: 'VSTestRunner', wait: true)
        powershell(returnStdout: true, script: 'scripts/HelloWaterWorld.ps1')
      }
    }
    stage('Deploy') {
      steps {
        powershell(script: 'TurnToStone.ps1', returnStdout: true)
      }
    }
  }
}