node {
    checkout scm

    docker.withRegistry('192.168.160.48:5000', '	dockerRegVM') {

        def customImage = docker.build("testapp-imagem")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}