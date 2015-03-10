# yiihttp
Change Display off Http ON Yii 2

UPDATE File : config/web.php IN 'components' array And add Source:

		'urlManager' => [
		  'showScriptName' => false,
		  'enablePrettyUrl' => true
		],    

ADD file : .htaccess IN folder WEB And add Source:

		RewriteEngine on
 
		# If a directory or a file exists, use it directly
		RewriteCond %{REQUEST_FILENAME} !-f
		RewriteCond %{REQUEST_FILENAME} !-d
		# Otherwise forward it to index.php
		RewriteRule . index.php

Your url now is like here : 
	http://localhost/yourapp/web/controller
