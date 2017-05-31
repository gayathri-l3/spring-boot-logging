node('maven') {
stage 'buildInprod'
openshiftBuild(buildConfig: 'springprod', showBuildLogs: 'true')
stage 'deployInprod'
openshiftDeploy(deploymentConfig: 'springprod')
openshiftScale(deploymentConfig: 'springprod',replicaCount: '1')
}
