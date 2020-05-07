# jenkinsTutorial
This repo is a simple project in which we will below components:
1) there are two branches of this repo 
 * master
 * dev1
2) We will be having jenkins and docker running in RHEL 8 where firewall is stopped.
3) We need to run two web servers in docker
  * production server 
  * Test server
3) The task of first jenkins item/job is to get the latest code change from master branch and put it directly into production server

### This is SCM configuration
![](images/job1_SCM.PNG)

### This is Build Trigger and Build configuration
![](images/job1_build.PNG)
5) The task of 2nd jenkins item/job is to get the latest change from dev1 branch and put it directly into test server.
### This is SCM configuration
![](images/job2_SCM.PNG)

### This is Build Trigger and Build configuration
![](images/job2_build.PNG)
6) The task of 3rd jenkins item/job is to run some automated test cases and only if the build is passed then dev1 branch should be merged to master branch and same should be reflected in production server
### This is SCM configuration
![](images/job3_SCM.PNG)
### This is Build Trigger
![](images/job3_buildTrigger.PNG)
### This is post build trigger configuration
![](images/job3_postBuild.PNG)
