node {
    // Ensure the desired Go version is installed
    def root = "go"

    // Export environment variables pointing to the directory where Go was installed
    
        
        stage 'Checkout'
        git url: 'https://github.com/miftahayuk/sample-go-jenkins.git'

        stage 'preTest'
        sh "${root} version"

        stage 'Test'
        sh "${root} test ./... -cover"

        stage 'Build'
        sh "${root} build ./..."
    
}