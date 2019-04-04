pipeline {
  agent any
  stages {
    stage('RunMatlab') {
      steps {
        timeout(unit: 'MINUTES', time: 15) {
          bat(script: '"%MATLAB_BASE%\\%MATLAB_VER%\\bin\\matlab.exe" -wait', encoding: 'UTF-8', returnStatus: true, returnStdout: true)
        }

      }
    }
  }
  environment {
    MATLAB_BASE = 'C:\\Program Files\\MATLAB'
    MATLAB_VER = 'R2018b'
  }
}