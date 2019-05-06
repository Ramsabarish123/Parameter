pipeline {
    agent any

    parameters {
        multi-line(name: 'MANIFESTS', defaultValue: '<?xml version="1.0" encoding="UTF-8"?>\n
<manifest>\n
    <remote name="origin" fetch="ssh://git@sdll9202.labs.teradata.com/source-code" />\n
    <default revision="16.60DRS_SLES11.3_experimental" remote="origin" sync-j="4" />\n
    <project name="tdbms" path="vob/dbsv2" />\n
    <project name="tvsa" path="vob/tvsa" />\n
    <project name="opnpde" path="vob/opnpde" />\n
    <project name="gateway" path="vob/gateway" />\n
    <project name="tdgss" path="vob/tdgss" />\n

    <project name="suselinux-x8664" path="vob/suselinux-x8664" />\n
    <project name="redhatlinux-x8664" path="vob/redhatlinux-x8664" />\n

    <project name="icu" path="vob/icu" />\n
    <project name="geospatial" path="vob/geospatial" />\n
    <project name="java" path="vob/java" />\n
    <project name="opnsrc" path="vob/opnsrc" />\n
    <project name="tdv" path="vob/tdv" />\n
    <project name="other" path="vob/" />\n
</manifest>')  
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
