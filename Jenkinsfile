node {
    checkout scm
    withCredentials([usernamePassword( credentialsId: 'dockerhub', usernameVariable: 'admindocker143', passwordVariable: '')]) {
        docker.withRegistry('http://registry.hub.docker.com', 'dockerhub') {

            def customImage = docker.build("admindocker143/dockerwebapp")

            /* Push the container to the custom Registry */
            customImage.push()
        }
    }
}
