## Global-Inspector
    

## Prerequisites
Make sure you have [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and [Docker desktop](https://www.docker.com/products/docker-desktop) installed.

## Installation 
Clone/git pull the repo into any local directory
```
git https://github.com/r-cemper/Global-Inspector.git
```
Run the IRIS container with your project: 
```
docker compose up -d && docker compose logs -f
```
## How to Test it

[http://localhost:42773/csp/user/webcmd.csp ](http://127.0.0.1:42773/csp/user/ginspect.CSP) 

### from Terminal Prompt 
To open IRIS Terminal do:
```
$ docker-compose exec iris iris session iris
USER>do ^rcc.ginspect
Global Name : %SYS
Maximum Subscripts : 2
Show content ? (0,1) [1] : 0
Start Subscript :"JOU"
Stop Subscript : "K"

^%SYS("JOURNAL")
^%SYS("JOURNAL","ALTDIR")
^%SYS("JOURNAL","CURDIR")
^%SYS("JOURNAL","CURRENT")
^%SYS("JOURNAL","EXPSIZE")
^%SYS("JOURNAL","LAST")
^%SYS("JOURNAL","MAXSIZE")
^%SYS("JOURNAL","PREFIX")
>>> stop <<<
USER>
```
or using **iTerm**   
[http://localhost:42773/iterm/](http://localhost:42773/iterm/)

To access IRIS System Management Portal:
[http://localhost:42773/csp/sys/UtilHome.csp](http://localhost:42773/csp/sys/UtilHome.csp)


[Article on DC](https://community.intersystems.com/)    
