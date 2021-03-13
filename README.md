# Updating-1.12-To-1.16.x
This is a guide on how to update your anarchy 1.12.2 client to a more recent version of Minecraft like 1.16.x. Seeing how 2b is experimenting with 1.16.4 and it seems to be going well we might see an a change from 1.12.2 to 1.16.4 on 2b and maybe more server will follow it. 

## Dont skip anything this is all really important

## Info
###### Im assuming you already have a "base" or "client" you want to do this with but if you dont this can still supply you with some good basics for using updated forge and mc. Im also assuming you have basic java and ide knowledge.


## Setup
To start off we want to clone our client so what i did was push my latest changes from my 1.12.2 version of the client to github. then you should create a new project using version control paste in the Git link then name it something so you know its the 1.16.x version. I named mine CousinWare1.16.x


## Gradle
Im hoping all of that went well and if it did you can continue to setup your gradle for minecraft 1.16.x. Im not good at gradle so maybe there are some places where you can clean up the code but below is going to be my gradle file(Gradle is not below its a file i posted on this repo). Anywhere where you see 'cousinware' in all lowercase is where you should put your modid. There will be places like in the picture below where you will want to change counsinware to your modid. This Gradle gets Minecraft 1.16.5 forge, Mixins for Minecraft and already sets them up(No MixinLoader Needed), and gets some extra things like Brady's or zeromemes EventManager. If your getting any errors try to run clean with gradle. Also you dont need to setupdecompworkspace re-importing gradle basically does this

![image](https://user-images.githubusercontent.com/56898064/111018614-7dd30a00-837f-11eb-9af6-7a176f9308ce.png)

## Mcmod.info
mcmodinfo isnt a thing anymore! there is a new way you can write descrptions about your mod in its mod page and specify its modid and such. Now go to your resources folder and make a folder in there called "META-INF"(This is where the new mcmodinfo thingy will go) Now Either create or paste the file in there. The File will be called mods.toml here you can set displayname, version, modid, desciption, authors, credits, logo file and many more. Also change the mod id and such to yours. The file should be located in this repo

## Main Class
As you can tell WOW everything is full of errors! dont worry this is going to be a really easy fix. First go ahead and do this so forge can recognize this as the main class you dont need to declare the MODID, NAME, and VERSION, but you must right above "public class CousinWare {" do @Mod(modid) Then you should do what i did in the second picture.
![image](https://user-images.githubusercontent.com/56898064/111018907-89bfcb80-8381-11eb-8225-4f8a86fbf739.png)
![image](https://user-images.githubusercontent.com/56898064/111019040-4ca80900-8382-11eb-8d5a-17b25cb0613f.png)

## Mapping
Alot changed from 1.12.2 to 1.16.5 so you're gonna have to do alot of remapping and such here is a link of old mappings to new mappings(Not all new mappings are there).
One more thing its not Minecraft.getMinecraft() its now Minecraft.getInstance()
https://gist.github.com/williewillus/2dfc945b7b7fdb69cc3ff830072d22fe

## Logging Into My Own Account
Go ahead and gen your intellijruns and go to run client and paste this into Program Arguments --username=(email) --password=(password)

## Issues
Forge is very buggy and weird so you might get alot of errors when trying to do things as the client starts up ie initialize settings which i ran into. I'd Also recommend to use Brady's Event Manager because before this i was using a different one causing my game to crash when i'd join a world

## Recommendations
If you want to check and see if this worked i would either move out a bunch of classes or comment them out(worry about the mc errors later) So you can fix your client to work with 1.16.5. Any other problems i reccomend messaging me on discord or just doing some research and looking at forge examples.
