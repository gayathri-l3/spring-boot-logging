node('maven') {
stage 'buildInDevelopment'
openshiftBuild(buildConfig: 'springprod', showBuildLogs: 'true')
stage 'deployInDevelopment'
openshiftDeploy(deploymentConfig: 'springprod')
openshiftScale(deploymentConfig: 'springprod',replicaCount: '1')
}
