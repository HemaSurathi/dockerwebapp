node {
    checkout scm
    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {

        def customImage = docker.build("firstl/docker_web_app")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
