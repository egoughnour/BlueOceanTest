pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build(propagate: true, job: 'VSTestRunner', wait: true)
        powershell 'scripts\\HelloWaterWorld.ps1'
      }
    }
  }
}