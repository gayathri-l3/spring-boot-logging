node('maven') {
stage 'buildInDevelopment'
openshiftBuild(buildConfig: 'springdev', showBuildLogs: 'true')
stage 'deployInDevelopment'
openshiftDeploy(deploymentConfig: 'springdev')
openshiftScale(deploymentConfig: 'springdev',replicaCount: '1')
}
