pipeline {
    agent any

    parameters {
        text(name: 'MANIFESTS', defaultValue: '<?xml version="1.0" encoding="UTF-8"?><manifest>  <remote name="origin" fetch="ssh://git@sdll9202.labs.teradata.com/source-code" />  <default revision="16.60DRS_SLES11.3_experimental" remote="origin" sync-j="4" />  <project name="tdbms" path="vob/dbsv2" />  <project name="tdbms" path="vob/dbsv2" />  <project name="tvsa" path="vob/tvsa" />  <project name="opnpde" path="vob/opnpde" />  <project name="gateway" path="vob/gateway" />  <project name="tdgss" path="vob/tdgss" />  <project name="suselinux-x8664" path="vob/suselinux-x8664" />  <project name="redhatlinux-x8664" path="vob/redhatlinux-x8664" />  <project name="icu" path="vob/icu" />  <project name="geospatial" path="vob/geospatial" />  <project name="java" path="vob/java" />  <project name="opnsrc" path="vob/opnsrc" />  <project name="tdv" path="vob/tdv" />  <project name="other" path="vob/" />  </manifest> ')
        string(defaultValue: "opnpde,tvsa,tdbms,tdgss,gateway", name: 'CHANGED_PROJECTS')
        string(defaultValue: "", name: 'TEST_PLAN')
        string(defaultValue: "Sles11.3", name: 'OS_VERSION')
        string(defaultValue: "16.60DRS_SLES11.3_stable", name: 'STABLE_BRANCH')
        string(defaultValue: "16.60", name: 'DBS_RELEASE')
        
    }

    stages {
        
        stage("BUILD") {
            steps {
                build job: 'Build', parameters: [string(name: 'MANIFESTS', value: '${params.MANIFESTS}') , string(name: 'CHANGED_PROJECTS', value: '${params.CHANGED_PROJECTS}')]
            }
        }
        
        stage("TEST") {
            steps {
                  echo "flag: ${params.CHANGED_PROJECTS}"
            }
        }
        
        
        
        
    }
}
