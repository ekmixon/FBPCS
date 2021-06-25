# How to build an OneDocker Image
| :point_down:  Make sure the prerequisites are satisfied   |
|-----------------------------------------|
## Prerequisites
* [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* [Docker](https://www.docker.com/get-started)
* [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-mac.html): 
* Open a terminal and run `aws configure` to setup credentials

## Steps
1. Clone the github repository
  `Git clone https://github.com/facebookresearch/FBPCS.git`
2. Change directory to onedocker
  `cd FBPCS/onedocker`
3. Build docker image
  `docker build . -t <docker_image_name>`
4. Tag the docker image (use `docker images` to get the image id)
  `docker tag <image_id> <ECR_url>`
6. Push the image to ECR
  `docker push <ECR_url>`
