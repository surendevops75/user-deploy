@Library('jenkins-shared-library') _

properties([
  parameters([
    string(name: 'appVersion', defaultValue: ''),
    string(name: 'deploy_to', defaultValue: 'dev')
  ])
])

def configMap = [
    project: "roboshop",
    component: "user",
    appVersion: (params.appVersion),
    deploy_to: (params.deploy_to)
]

echo "Going to execute Jenkins shared library"
echo "ConfigMap: ${configMap}"

EKSDeploy(configMap)