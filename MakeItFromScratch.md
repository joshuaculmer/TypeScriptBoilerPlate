So you've decided to download the boilerplate but really want to own it, know how it works, and what everything does. You have my respect. Included in this simple guide is everything that you'll need to know to start your own Typescript Boilerplate from the ground up.
### Disclaimer 

I make a couple of assumptions throughout this guide:
1. You have basic programming experience
2. You are comfortable with the terminal
3. You have little to no knowledge of TypeScript
4. Your IDE does not wig out and/or behaves like VS Code, which is what I am using

I am also making this guide for my own reference, it is designed so that I can go back and reference it at anytime, with the details that I am most likely to forget, not with what I think will be most useful for absolute beginners. 
## Download Node.js

Ight so you'll need to download Node to get started. Go to their website and download the basic one for windows without all the Docker configurations, this guide won't go into Docker.

https://nodejs.org/en/download

Once you have downloaded Node, confirm from your terminal that it was installed correctly. Type npm -v to confirm the version is up to date.

Node allows us to use JavaScript outside of a browser and we will be using NPM or Node Package Manager a lot throughout the project.

### A note on updating node
Updating node to the most recent version, for me it was 11.5.2, broke npm's ability to run as a script. I just changed the policy level  
	Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Basically only allows signed remote scripts to run, npm is signed, so it runs. Does not effect local scripts, so be careful if you download a malicious script it may be considered local and run anyways.

## Configure Node

Within your project location begin the node project.
	npm init --yes
This should have created a package.json file

We'll also want to configure out Node project to compile TypeScript
	npm install typescript --save-dev
This should have added folder called node_modules with a lot of files in it. This folder contains all the dependencies that your project uses.

Next add node types 
	npm install @types/node --save

And we'll finish off with adding a configuration for your TypeScript Commpiler
	npx tsc --init
You should see a file tsconfig.json added. This file containts all the compiler settings for your project. 