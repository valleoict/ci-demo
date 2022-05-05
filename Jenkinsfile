pipeline{
    agent any
	tools {
        maven 'maven-3.6.3'
        jdk 'jdk8'
    }
    stages{
        stage('init'){
            steps{
                script{
                    println("Hello world")
                }
            }
        }
		 stage('Build') {
            steps {
				script{
					dir('maven_project'){
					sh 'mvn -B -DskipTests clean package' }
				}
            }
        }
		 stage('Test') {
            steps {
				script{
					dir('maven_project'){
					sh 'mvn test' 
					}
				}
            }
        }
    }
}
