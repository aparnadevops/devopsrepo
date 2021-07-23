pipeline {
    agent any
    
    parameters {
        choice(name: 'Platform',choices: ['abc', 'xyz'], description: 'Target OS platform', )
        string(name: 'platform2', defaultValue: 'xyz', description: '')
    }

    stages {
        stage('Hello') {
            steps {
                triggerRemoteJob remoteJenkinsName: 'http://ip172-18-0-120-c3ta8bnnjsv000ctucr0-8080.direct.labs.play-with-docker.com/', job: 'trigger remotely', blockBuildUntilComplete: true
                echo 'hello world'
            }
        }
    }
}
