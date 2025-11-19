pipeline {
    agent any
    stages {
        stage('Run Frontend') {
            steps {
                echo "Executing yarn..."
                nodejs('Node-25.2') {
                    sh 'yarn install'
                }
            }
        }

        stage('Run Backend') {
            steps {
                echo "Executing Gradle..."
                withGradle(gradleName: 'Gradle') {
                    sh './gradlew -v'
                }
            }
        }
    }
}
