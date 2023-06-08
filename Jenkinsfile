    def userGit = "bibee"
    def userDocker = "babibe2211"
    def repository = "https://github.com/bibeee/clone-ldp"
    def dockerRegistry = "https://registry.hub.docker.com"
    def branch = "main"
    def prj = "ldp"
    node("jenkins-agent") {
            stage("Pull code from GitLab"){
                    git branch: "${branch}", credentialsId: "${userGit}", url: "${repository}"
            }
            stage ("Build code") {
                customImage = docker.build("${userDocker}/${prj}:${BUILD_ID}")
             
            }
            stage ("Push code") {
                withDockerRegistry([url: "", credentialsId: "${userDocker}"]) {
                customImage.push()   
            }

            }
        // }
    }

