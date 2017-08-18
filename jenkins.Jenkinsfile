node {
    // Clean workspace before doing anything
    deleteDir()

    try {
        stage ('Clone') {
            checkout scm
        }
        stage ('Build') {
           
        }
        stage ('Tests') {
            parallel 'static': {
              
            },
            'unit': {
               
            },
            'integration': {
               
            }
        }
        stage ('Deploy') {
           
        }
    } catch (err) {
        currentBuild.result = 'FAILED'
        throw err
    }
}