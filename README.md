# Updating-1.12-To-1.16.x
This is a guide on how to update your anarchy 1.12.2 client to a more recent version of Minecraft like 1.16.x. Seeing how 2b is experimenting with 1.16.4 and it seems to be going well we might see an a change from 1.12.2 to 1.16.4 on 2b and maybe more server will follow it.



## Info
###### Im assuming you already have a "base" or "client" you want to do this with but if you dont this can still supply you with some good basics for using updated forge and mc. Im also assuming you have basic java and ide knowledge.


## Setup
To start off we want to clone our client so what i did was push my latest changes from my 1.12.2 version of the client to github. then you should create a new project using version control paste in the Git link then name it something so you know its the 1.16.x version. I named mine CousinWare1.16.x


## Gradle
Im hoping all of that went well and if it did you can continue to setup your gradle for minecraft 1.16.x. Im not good at gradle so maybe there are some places where you can clean up the code but below is going to be my gradle file. Anywhere where you see 'cousinware' in all lowercase is where you should put your modid. There will be places like in the picture below where you will want to change counsinware to your modid.

![image](https://user-images.githubusercontent.com/56898064/111018614-7dd30a00-837f-11eb-9af6-7a176f9308ce.png)

