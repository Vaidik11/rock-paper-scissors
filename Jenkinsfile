node {
    stage('Version') { 
        echo "Checking version..."
        bat "mvn -v"
    }

    stage('Environment') {
        echo "Checking environment..."
    }

    stage('Document') {
        echo "Skipping Javadoc for now"
    }

    stage('Compile') {
        echo "Compiling project..."
        bat "mvn clean verify"
    }

    stage('Acceptance') {
        echo "Acceptance tests (manual step skipped)"
    }

    stage('Almost Done!') {
        def response = input message: 'Whatcha think?', 
            parameters: [choice(choices: 'Yes\nNo', description: 'Proceed or Abort?', name: 'Wasn\'t that cool?')]
        
        if (response == "Yes") {
            echo "I agree!"
        } else {
            echo "You are hard to please."
        }
    }

    stage('Static Code Analysis') {
        echo "Static analysis placeholder (SonarQube/Checkstyle can go here)"
        // Later you can integrate SonarQube or Checkstyle:
        // bat "mvn sonar:sonar"
    }
}
