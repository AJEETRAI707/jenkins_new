pipeline {
    agent {
        docker { image 'ubuntu' }
	}

     environment {
         withCredentials([usernamePassword(credentialsId: 'e9d8459c-a4d8-4325-8b04-266075ab3a4b', usernameVariable: 'Username', passwordVariable: 'Password')])
     }

    stages {
        stage('Run') {
        steps {
		
// 		 environment {

//    withCredentials([usernamePassword(credentialsId: 'docker_login', usernameVariable: 'username1', passwordVariable: 'password1')])

//     }
// 		
        sh 'set -x'
        echo "Hello !!"
        echo 'username is ${username}'
        echo 'Password is ${password}'
        sh 'git status'\
        


		// docker.withRegistry('', 'docker-hub-credentials') {
	     sh "docker login -u ${username1} -p ${password1}"
         sh "lsblk"
		// myImage.push("${env.BUILD_NUMBER}")
		// myImage.push("latest")		

	//	sh 'docker --version'

                sh "echo $username"
                sh "echo $password"
            }
        }
    }
  }
