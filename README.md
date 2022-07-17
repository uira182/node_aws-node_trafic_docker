## DOCKER - NODEJS - TRAFIC - AWS

## 1º AWS INSTALL AND CONFIGURE
- Install aws cli: https://aws.amazon.com/pt/cli/
- Run code: aws configure
- Fill in the information
- open port: 80 and 8080.

## 2º DOCKER-MACHINE INSTALL AND CONFIGURE
- Install docker-machine: https://docs.docker.com/desktop/
- Run code: docker-machine create --driver amazonec2 aws01
- Run code: docker-machine env aws01
- Run code: eval $(docker-machine env aws01)

Now we are directly connected to aws and all commands will run in our instance.

## 3º UPDATE FILES
 - ./docker-production.yml - fill in your domain

## RUN APP
- run code: docker-compose up - to test and enter in the your site http://yourdomain.com:3000
- to exit press [ ctrl ] + [ c ]
- run code: docker-compose -f docker-compose.yml -f docker-production.yml up -d
- run code: docker ps - to view your running container

## TERMINAL EXIT AWS
- run code: eval $(docker-machine env -u)



