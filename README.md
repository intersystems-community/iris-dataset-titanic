## iris-dataset-titanic
This repository contains a class and data of Titanic passengers in a Global

## Prerequisites
Make sure you have [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and [Docker desktop](https://www.docker.com/products/docker-desktop) installed.

## Installation 

zpm "install dataset-titanic"

## Development

Clone/git pull the repo into any local directory

```
$ git clone https://github.com/intersystems-community/objectscript-docker-template.git
```

Open the terminal in this directory and run:

```
$ docker-compose up -d
```

## How to Test it

In IRIS terminal:

```
$ docker-compose exec iris iris session iris
USER>D $System.SQL.Shell()
[SQL]USER>>Select * from dc_data.Titanic
...
890     890     1       1       Behr, Mr. Karl Howell   male    26      0       0       111369  30       C148    C
891     891     0       3       Dooley, Mr. Patrick     male    32      0       0       370376  7.75             Q

891 Rows(s) Affected
statement prepare time(s)/globals/cmds/disk: 0.2047s/51607/268016/0ms
          execute time(s)/globals/cmds/disk: 0.1058s/892/161300/0ms
                          cached query class: %sqlcq.USER.cls8
```

## In InterSystems SQL Tools in VSCode
Open repo in VSCode (see develoment above)
Install [InterSystems SQLTools](https://marketplace.visualstudio.com/items?itemName=intersystems-community.sqltools-intersystems-driver)

Use the connection "iris-dataset-titanic"

Open dc.data.Titanic table and see the records:
<img width="968" alt="Screenshot 2021-01-21 at 13 33 53" src="https://user-images.githubusercontent.com/2781759/105340135-8e23ff80-5bee-11eb-9e5e-ff87dfdab047.png">


## How to start coding
This repository is ready to code in VSCode with ObjectScript plugin.
Install [VSCode](https://code.visualstudio.com/), [Docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker) and [ObjectScript](https://marketplace.visualstudio.com/items?itemName=daimor.vscode-objectscript) plugin and open the folder in VSCode.
Open /src/cls/PackageSample/ObjectScript.cls class and try to make changes - it will be compiled in running IRIS docker container.
![docker_compose](https://user-images.githubusercontent.com/2781759/76656929-0f2e5700-6547-11ea-9cc9-486a5641c51d.gif)

Feel free to delete PackageSample folder and place your ObjectScript classes in a form
/src/Package/Classname.cls
[Read more about folder setup for InterSystems ObjectScript](https://community.intersystems.com/post/simplified-objectscript-source-folder-structure-package-manager)

The script in Installer.cls will import everything you place under /src into IRIS.

