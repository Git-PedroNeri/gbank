# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
* [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/2.5.6/maven-plugin/reference/html/)
* [Create an OCI image](https://docs.spring.io/spring-boot/docs/2.5.6/maven-plugin/reference/html/#build-image)
* [Spring Web](https://docs.spring.io/spring-boot/docs/2.5.6/reference/htmlsingle/#boot-features-developing-web-applications)
* [Spring Data JPA](https://docs.spring.io/spring-boot/docs/2.5.6/reference/htmlsingle/#boot-features-jpa-and-spring-data)

### Guides
The following guides illustrate how to use some features concretely:

* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/bookmarks/)
* [Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)
* [Connecting to GitHub with SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)
* [Git - guia prático](http://rogerdudler.github.io/git-guide/index.pt_BR.html)
* [Documentando uma API Spring Boot com o Swagger](https://www.treinaweb.com.br/blog/documentando-uma-api-spring-boot-com-o-swagger)


### Install Developer Guide

#### Prerequisite

- git (you can download it in https://git-scm.com/downloads)
- jdk 8 ( you can download it in https://docs.aws.amazon.com/corretto/latest/corretto-8-ug/downloads-list.html)
- Defined JAVA_HOME enrivonment variable in your system
- ssh 


#### Steps

##### Generate your SSH Key

To connect to a Git server securely you need to generate an SSH Key (public and private key). This key must be registered on Github in order to have access to the project repositories. Follow the steps in : [Conectar-se ao GitHub com SSH](https://docs.github.com/pt/authentication/connecting-to-github-with-ssh)

ATTENTION: After generating your public and private key, keep a copy in a safe place for later use if you have any problems

TIP: Add Github in Know Hosts

    ssh-keyscan github.com >> ~/.ssh/known_hosts

  ##### Clone the git repository
  
    git clone git@github.com:GBank-1/gbank.git
  
  ##### Go into project folder
  
    cd gbank
  
  
  ##### Setting up Git
  
   Set your username in Git whith the same on Github Account
   
     git config user.name "Mona Lisa"
    
   Set your email in Git whith the same on Github Account
    
     git config user.email "email@email.com"
  
   TIP: If you use more than one ssh key, you can specify the key to use
  
     git config core.sshCommand 'ssh -i ~/.ssh/id_ed25519_2.pub'
  
  ##### Execute the goals' maven:
  
  - build:
  
           .\mvnw clean install 
  
  - deploy in embedded tomcat:
  
          .\mvnw spring-boot:run
  
  Note: You could need before run it, in linux System, get execution permission for mvnw file
  
  
  
  ##### Api Doc:
  
  [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)




