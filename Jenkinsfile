node {
    checkout scm
    docker.withRegistry('https://registry.hub.docker.com/repository/docker/khoicrtp/mmtnc_2021', 'dockerhub') {
        def customImage = docker.build(test4)//("my-image:${env.BUILD_ID}")
        //def customImage = docker.build("cicdjenkins")
        /* Push the container to the custom Registry */
        customImage.push()
	}
}