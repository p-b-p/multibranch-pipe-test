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
                        'return[\'err\']'
                ],
                script: [
                    classpath: [],
                    sandbox: false,
                    script:
"""def a = ['BBP', 'BCT', 'PBP']
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
    stage('Test') {
      steps {
        script {
          def jstring = '{"one":1, "two":2}'
          def jobj = readJSON text: jstring
          echo jobj.toString()
        }
      }
    }
  }
}
