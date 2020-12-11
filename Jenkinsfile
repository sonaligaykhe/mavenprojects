pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven"
        jdk "Java"
        
    }

    stages {
        stage('SCM Checkout') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/sonaligaykhe/mavenprojects.git'
            }
        }
        
        stage('Compile Stage') {
            steps {
                sh 'mvn -f myproject123/multi-module/pom.xml clean package'
                echo 'Build Compile Successful'
            }
        }
        
        stage('Build') {
            steps {
                sh 'mvn install'
                echo 'Build Complete'
            }
        }
    }
}
