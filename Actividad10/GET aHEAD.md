### 🚩 [GET aHEAD ]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
Find the flag being held on this server to get ahead of the competition

**Solución:**  
`┌──(kali㉿kali)-[~]
└─$ curl -s -X HEAD http://wily-courier.picoctf.net:58230/index.php 
           
┌──(kali㉿kali)-[~]
└─$ curl -s -i http://wily-courier.picoctf.net:58230/index.php      

HTTP/1.1 200 OK
Date: Mon, 07 Sep 2026 16:23:13 GMT
Server: Apache/2.4.38 (Debian)
X-Powered-By: PHP/7.2.34
Vary: Accept-Encoding
Content-Length: 1064
Content-Type: text/html; charset=UTF-8


<!doctype html>
<html>
<head>
    <title>Red</title>
    <link rel="stylesheet" type="text/css" href="//maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">
        <style>body {background-color: red;}</style>
</head>
        <body>
                <div class="container">
                        <div class="row">
                                <div class="col-md-6">
                                        <div class="panel panel-primary" style="margin-top:50px">
                                                <div class="panel-heading">
                                                        <h3 class="panel-title" style="color:red">Red</h3>
                                                </div>
                                                <div class="panel-body">
                                                        <form action="index.php" method="GET">
                                                                <input type="submit" value="Choose Red"/>
                                                        </form>
                                                </div>
                                        </div>
                                </div>
                                <div class="col-md-6">
                                        <div class="panel panel-primary" style="margin-top:50px">
                                                <div class="panel-heading">
                                                        <h3 class="panel-title" style="color:blue">Blue</h3>
                                                </div>
                                                <div class="panel-body">
                                                        <form action="index.php" method="POST">
                                                                <input type="submit" value="Choose Blue"/>
                                                        </form>
                                                </div>
                                        </div>
                                </div>
                        </div>
                </div>
        </body>
</html>
┌──(kali㉿kali)-[~]
└─$ curl -s -I http://wily-courier.picoctf.net:58230/index.php 

HTTP/1.1 200 OK
Date: Mon, 07 Sep 2026 16:23:41 GMT
Server: Apache/2.4.38 (Debian)
X-Powered-By: PHP/7.2.34
flag: picoCTF{r3j3ct_th3_du4l1ty_8b13f07}
Content-Type: text/html; charset=UTF-8

┌──(kali㉿kali)-[~]
└─$ 
`
`


[picoCTF{r3j3ct_th3_du4l1ty_8b13f07}
