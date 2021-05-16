node {
    checkout scm

    // 192.168.160.48:5000 | regCert
    /*
      1º arg -> URL do registry
      2º arg -> ID da credencial (pode não ser passado)
    */
    // 'https://registry.hub.docker.com/', 'dockerhub'
    docker.withRegistry('192.168.160.48:5000') {

        /*
          1º arg -> nome da imagem: neste caso é o meu username (alexandrejflopes) /<nome da imagem>
          2º arg -> caminho, no repositório, do Dockerfile da imagem a construir (pode não ser passado)
        */
        // "alexandrejflopes/testapp-image", "./testapp"
        def customImage = docker.build("192.168.160.48:5000/testapp-image", "./testapp")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}