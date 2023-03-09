properties([
    parameters([
        [$class: 'ChoiceParameter',
            choiceType: 'PT_SINGLE_SELECT',
            description: 'Bitbucket project key',
            filterLength: 1,
            filterable: false,
            name: 'PROJECT_KEY',
            script: [
                $class: 'GroovyScript',
                fallbackScript: [
                    classpath: [],
                    sandbox: false,
                    script:
                        'return[\'ups\']'
                ],
                script: [
                    classpath: [],
                    sandbox: false,
                    script:
                        """println("PBP")"""
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
  }
}
