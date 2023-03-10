properties([
    parameters([
        [$class: 'ChoiceParameter',
            choiceType: 'PT_SINGLE_SELECT',
            description: 'Bitbucket project key',
            filterLength: 1,
            filterable: false,
            name: 'PROJECT_KEY',
            randomName: 'choice-parameter-7108218389296307',
            script: [
                $class: 'GroovyScript',
                fallbackScript: [
                    classpath: [],
                    sandbox: false,
                    script:
"""return[\'ups\']"""
                ],
                script: [
                    classpath: [],
                    sandbox: false,
                    script:
"""def a = ["BbB", "BcT", "BrC"]
return a.reverse(true)"""
                ]
            ]
        ]
    ])
])

pipeline {
  agent any
  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
  }
  stages {
    stage('Hello') {
      steps {
        sh '''
          java -version
        '''
      }
    }
    stage('cat README') {
      when {
        branch "dev-*"
      }
      steps {
        sh '''
          cat README.md
        '''
      }
    }
  }
}
