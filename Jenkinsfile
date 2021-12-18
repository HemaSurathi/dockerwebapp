node {
    checkout scm
    withCredentials([usernamePassword( credentialsId: 'dockerhub', usernameVariable: 'admindocker143', passwordVariable: 'Kalpakkam1479')]) {
        docker.withRegistry('http://registry.hub.docker.com', 'dockerhub') {

            def customImage = docker.build("firstl/docker_web_app")

            /* Push the container to the custom Registry */
            customImage.push()
        }
    }
}
