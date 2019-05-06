pipeline {
    agent any

    parameters {
        text(name: 'MANIFESTS', defaultValue: "HELLO mon")  
        string(defaultValue: "opnpde,tvsa,tdbms,tdgss,gateway", name: 'CHANGED_PROJECTS')
        string(defaultValue: "", name: 'TEST_PLAN')
        string(defaultValue: "Sles11.3", name: 'OS_VERSION')
        string(defaultValue: "16.60DRS_SLES11.3_stable", name: 'STABLE_BRANCH')
        string(defaultValue: "16.60", name: 'DBS_RELEASE')
        
    }

    stages {
        
        stage("foo") {
            steps {
                echo "flag: ${params.MANIFESTS}"
            }
        }
        
        
        
        
    }
}
