pipeline{
	agent any{
	stages{
	stage ("FetchCodeFromGit"){
	steps{
	git credentialsId: '73b7f0ff-4a86-43e9-93d8-d2ffb53f498a', url: 'https://github.com/Raja6865/Sample_Project.git'
	}
	stage ("Build"){
	steps{
	sh 'mvn clean package'
	}
	}
	stage ("Deploy"){
	steps{
	deploy adapters: [tomcat9(credentialsId: 'ce1d19fb-1b2d-4b6b-8a64-2eed7af87a3f', path: '', url: 'http://3.6.126.158:8081/')], contextPath: null, war: '**/simple-web-app.war'
	}
	}
	}
	}
	}
}
