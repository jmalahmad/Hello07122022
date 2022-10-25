pipeline {
    agent any
    tools{ 
	    jdk 'Java 11' 
	}
    environment { JAVA_HOME = '/usr/lib/jvm/java-11-openjdk-amd64/' }
    stages {
        stage ('Compile Stage') {
            steps {
                withMaven(maven : 'Maven 3.8.6') {
                    sh 'mvn clean compile'
                }
            }
	}
	stage ('Testing Stage') {
            steps {
                withMaven(maven : 'Maven 3.8.6') {
                    sh 'mvn test'
                	}
		}
	}
        stage ('Install Stage') {
            steps {
                withMaven(maven : 'Maven 3.8.6') {
                    sh 'mvn install'
                } 
            } 
        } 
     }
 }

