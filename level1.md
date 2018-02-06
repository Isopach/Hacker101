# Level 1: Breakbook


```
		In this level, there are 4 vulnerabilities, falling into the following classes:
		CSRF
		Stored XSS
		Forced Browsing

		Have fun!
```
    

## Forced Browsing:    

`https://levels-a.hacker101.com/levels/1/post?id=88`      
Change post ID to view anyone's post & their gmail IDs      
![Forced Browsing](https://github.com/Isopach/Hacker101/blob/master/img/level1_forced_browsing.png)

---- 

## Reflected XSS:       

Post a HTTP link with a delimiter like `"` or `*`     
`http://test.com/"onmouseover="alert('hakd')`        

![Reflected XSS](https://github.com/Isopach/Hacker101/blob/master/img/level1_stored_xss.png)

----
  
## CSRF:    
Token is exposed in source. Not sure what can I do with it unless I manage to obtain someone else's token
