pipeline {
  agent any
  stages {
    stage('YARN') {
      steps {
        sh 'yarn install'
        sh 'yarn'
        sh './node_modules/.bin/bazel build :bundle'
        sh 'node bazel-bin/bundle.js'
      }
    }
  }
}
