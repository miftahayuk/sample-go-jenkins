node {
    // Ensure the desired Go version is installed
    def root = tool type: 'go', name: 'go1.13.8'

    // Export environment variables pointing to the directory where Go was installed
    withEnv(["GOROOT=${root}", "PATH+GO=${root}/bin"]) {
        
        stage 'Checkout'
        git url: 'https://github.com/miftahayuk/sample-go-jenkins.git'

        stage 'preTest'
        sh 'go version'

        stage 'Test'
        sh 'go test -cover'

        stage 'Build'
        sh 'go Build'

        stage 'Deploy'
    }
}