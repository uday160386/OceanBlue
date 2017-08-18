node {
    // Clean workspace before doing anything
    deleteDir()

    try {
        stage ('Clone') {
            checkout scm
        }
        stage ('Build') {
        parallel 'DEV':{
        
        },
        'SIT'{
        },
        'UAT'{
        }
        'PROD'{
        }
           
        }
        stage ('Unit') {
            parallel 'unit': {
              
            },
           'integration': {
               
            }
            
        }
        
         stage ('Functional UI Tests') {
        parallel 'Android:{
            }
            'iOS'{
            }
        stage ('Deploy') {
        
         parallel 'DEV':{
        
        },
        'SIT'{
        },
        'UAT'{
        }
        'PROD'{
        }
           
        }
    } catch (err) {
        currentBuild.result = 'FAILED'
        throw err
    }
}