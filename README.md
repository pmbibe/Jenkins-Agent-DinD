# Jenkins-Agent-DinD
1. Setup Jenkins
2. Add Node and Clouds Jenkins
  - Config Docker Clould
    - Set Docker Host URI (Use tcp://)
    - Enabled 
  - Config Docker Agent templates
    - Set Label 
    - Enabled
    - Set Name
    - Set Docker Image: eeacms/jenkins-slave-dind
    - Set Env in Container settings: DOCKER_HOST=tcp://
    - Connet method: Attach Docker container
