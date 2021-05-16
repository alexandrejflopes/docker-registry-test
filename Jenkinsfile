node {
    checkout scm

    docker.withRegistry('192.168.160.48:5000', 'dockerRegVM') {

        def customImage = docker.build("alexandrejflopes/testapp-image", "./testapp")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}