node('maven') {
stage 'buildInDevelopment'
openshiftBuild(namespace: 'development', buildConfig: 'springdev', showBuildLogs: 'true')
stage 'deployInDevelopment'
openshiftDeploy(namespace: 'development', deploymentConfig: 'springdev')
openshiftScale(namespace: 'development', deploymentConfig: 'springdev',replicaCount: '2')
stage 'deployInTesting'
openshiftTag(namespace: 'production', buildConfig: 'springprod', showBuildLogs: 'true')
openshiftDeploy(namespace: 'production', deploymentConfig: 'springprod', )
openshiftScale(namespace: 'production', deploymentConfig: 'springprod',replicaCount: '3')
}
