# Devops project



## Table of content



1. [Front](#Front)
2. [Back](#Back)
3. [Docker-compose](#docker-compose)



### Front



The front end of our projet have been released in rust. It s a simple front end that display hello world, and have some test.

We added a git hub action that is stored in the .github/workflows/rust.yml.



The Ci is launched every time we push on the main branch (master now).



![image-20201114094952004](/Users/james/Library/Application Support/typora-user-images/image-20201114094952004.png)



The test of the code are stored in the file src/main.rs



The Dockerfile is inside the project folder.



### Back



The back end of our project have been released in Node js.

It s a simple Koa app listening on 3000 port.

We added to this project a git hub action that ll launch the ci and the test before pushing on master.



![image-20201114095613908](/Users/james/Library/Application Support/typora-user-images/image-20201114095613908.png)



The Dockerfile is inside the project folder.



### Docker-compose

Our docket compose ll build the front end and the back end along side the database. The database is a mongodb database.

Variable for the configuration of the database are stored in the .env file

The dockercompose ll go inside the front end and the back end folder to build them, it ll create a network between the database and the backend && the backend and the frontend.