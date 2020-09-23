<div align="center">

## True HTML/JavaScript Source Hiding


</div>

### Description

After many months of "No right click" and "Popup"

experimenting I have compiled this method of what I belive is an unbreakable routine for producing secure web pages. It is a combination of ASP/Javascript and html encryption.
 
### More Info
 
You must have an ASP enabled server for this to work.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Leon Hosie](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/leon-hosie.md)
**Level**          |Intermediate
**User Rating**    |5.0 (20 globes from 4 users)
**Compatibility**  |
**Category**       |[Security](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/security__2-74.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/leon-hosie-true-html-javascript-source-hiding__2-2379/archive/master.zip)





### Source Code

```
This method requires you to have a start page. This can be a flash presentation or just a click through link. It does not support OnLoad Popups as it works from the Referring URL.
<!-- Step 1.
Create your start page in html. My code is below if you wish to get the idea:
-->
<html>
<HEAD>
<TITLE>Start Page</TITLE>
</HEAD>
<BODY text="#336699" link="#ffffff" vlink="ffffff" alink="ffffff">
<center>
<a href="http://voicecafe.optecs.net" border="0">
<img src="http://voicecafe.optecs.net/images/ccup.jpg"></a><br><br>
<font size="5" face="Georgia"><b>Web-based Communication</b></font>
<br><font size="4" face="Georgia"><b>by OpTecs</b></font><br><br><br>
<a href="http://www.yourdomain.com/check_refer.asp">
<font size="5" color="#336699"><b>Please click here to go to the Protected Page</a>
</BODY>
</HTML>
<!-- Step 2.
Save this page as: startpage.html
Then Encrypt this page with the HTMLcrypt.exe program.
Download here: ftp://ftp.cedium.net/internet/htmlcrypt/encryptHTML.exe
-->
<!-- Step 3.
create your protected page. Start with standard html or javascript.
This is my page:
-->
<html>
<title>Secure Source Code Page</title>
</head>
<body bgcolor="#ffffff" topmargin="0" leftmargin="0">
<center>
<font size="5" color="#336699">Try and link directly to this page.</font>
</body>
</html>
<!-- Step 4.
Save this page as: check_refer.html
Now encrypt this page using the HTMLcrypt program.
Step 5. Now open check_refer.html in your html editor and insert this code above the <html> tag:
-->
<%
dim u_file
u_file = request.servervariables("http_referer")
if u_file <> "http://www.yourdomain.com/startpage.html
response.redirect "http://www.interpol.com/Public/TechnologyCrime/default.asp"
response.end
else %>
<html>
<!-- Now add this code below the </html> tag: -->
</html>
<% end if %>
<!-- Step 6.
Save check_refer.html as check_refer.asp and upload both files to your server.
-->
To test simply try and go directly to check_refer.asp
and you should be redirected to the Interpol site... 8) (you may redirect to any page you wish).
<!-- Go to this URL for an example: http://voicecafe.optecs.net/securitytest/voice.html
-->
NB. The HTMLcrypt program allows you to disable the right click and the view source will show the encrypted html.
If you have any questions please contact me.
Thanks to Cedium.net for the great freeware.
```

