# Blockchain Lab 01
## Introduction

## Requisites
* _git_ installed
* _NodeJS_ installed
* _yarn_ installed

## Instructions

### Prepare project folder
We must prepare our project folder to store a NodeJS application. For that the best approach is to initialize our directory with the required files.

1. **Create project folder** 

Go to your projects root folder and create a project folder
```bash
user:/home/user$ mkdir lab01
user:/home/user$ cd lab01
user:/home/user/lab01$
```

2. **Initialize project with yarn**

Let's invoke yarn to initialize our `package.json` file
```bash
user:/home/user/lab01$ yarn init
name (your-project): lab01
description: My first laboratory on blockchain
entry point (index.js):
git repository:
author:
license (MIT):
```
That sould create a `package.json` file with all the information about our project

```json
{
  "name": "lab01",
  "version": "1.0.0",
  "description": "My first laboratory on blockchain",
  "main": "index.js",
  "author": "",
  "license": "MIT"
}
``` 

3. **Basic project initialitation stuff**

Now you should have an empty _NodeJS_ project with _yarn_ as the dependency manager. Once done this, let's make some minor adjustments:

   1. ***Initialize version control***

   Now it's time to add our project to _git_ to manage our code. In the root folder use _git_ to initialize the version control

   ```bash
   user:/home/user/lab01$ git init
   ...
   user:/home/user/lab01$ git add .
   ...
   user:/home/user/lab01$ git commit -m "First version"
   ...

   ``` 

   Now your project files should be under _git_ control allowing you to be protected from mistakes or accidental deletions. 

   > **NOTE** If your project is going to be developed betweem several people,  you should consider to _pull_ your repo to a remote repo like _Visual Studio Team Services_, _GitHub_ or _GitLab_. If so, please read _git_ documentation about [Working with remote repos](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes)

   1. ***Create .gitignore file***

   `.gitignore` file helps us to exclude those files that we don't want to set under _git_ control. For example, usually most users exclude _node_ package dependencies for source control. To do this, create a file _.gitignore_ in your project root folder:

   ```bash
   user:/home/user/lab01$ touch .gitignore
   user:/home/user/lab01$ echo "node_modules/" >> .gitignore
   user:/home/user/lab01$ git add .gitignore
   user:/home/user/lab01$ git commit -m "Added .gitignore to project"
   ...
   ```
   2. ***Add first dependencies to the project***

   As said before, _yarn_ will manage our packages dependencies. In order to work with blockchain (ethereum) we are going to add this dependencies to our project

   ```bash
   $ yarn global add ganache-cli 
   $ yarn add truffle --dev
   ``` 
