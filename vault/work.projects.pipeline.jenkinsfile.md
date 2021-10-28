---
id: 9e7dac84-1d1b-4327-8c12-f7b2b9c4a220
title: Jenkinsfile
desc: ''
updated: 1617654459594
created: 1617654431558
---

```groovy
def label = "mypod-${UUID.randomUUID().toString()}"
// These only need to be uncommented if the differ from the defaults
// // Unit Test Health Score: 1 - 100 (defaults to 50)
def healthScore = 0
// // runCoverage
def runCoverage = false
// // Lint fail count (dafaults to 100)
def failLimit = 0

podTemplate(label: label, serviceAccount: "jenkins", containers: [
  containerTemplate(name: 'node', image: "node:${NODE_VERSION}", command: 'cat', ttyEnabled: true),
  containerTemplate(name: 'docker', image: 'docker', command: 'cat', ttyEnabled: true),
  containerTemplate(name: 'helm', image: 'lachlanevenson/k8s-helm:v2.10.0', command: 'cat', ttyEnabled: true),
  containerTemplate(name: 'jq', image: 'stedolan/jq', command: 'cat', ttyEnabled: true)
],
volumes: [
  hostPathVolume(mountPath: '/var/run/docker.sock', hostPath: '/var/run/docker.sock')
]) {
  node(label) {
    stage('load pipeline'){ 
        pipeline = fileLoader.fromGit(
            'microservice-1.0.0',
            'https://github.com/TheWeatherCompany/wsi-media-engage-jenkins.git',
            'master',
            'JenkinsGithub',
            label
        )
    }
    // 
    pipeline.runJenkinsfile(healthScore, runCoverage, failLimit)
  }
}
```