# Global-Inspector
If you are investigating complex structured Globals this can become  
a rather boring typing exercise. Different from Global Explorer in   
System Management Portal Global-Inspector allows a kind of drill-down   
to dig deeper and deeper by subscript levels.  
You also have the option to see the stored content or to show only   
the subscript structures.    
Globals storing SQL Tables are probably not so thrilling, but in SYSTEM   
space you find real trees with completely different branches and twigs.  

Global-Inspector can run in browser or from terminal command line.

**required input**   
- Global name: with or without leading caret   
- Maximum number of subscripts you want to see  
- Showing content of the displayed Global node   
- Starting Subscript. Can be exact or before first node shown     
- Stopping Subscript. Can be exact or before first node excluded  
      
Subscripts require exact quoting. E.g. "JOURNAL" not JOURNAL    
 
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
[http://localhost:42773/csp/user/ginspect.CSP](http://localhost:42773/csp/user/ginspect.CSP)

<img width="468" height="450" alt="image" src="https://github.com/r-cemper/Global-Inspector/blob/main/browser.jpg" />  

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

[Article on DC](https://community.intersystems.com/post/global-inspector)     
