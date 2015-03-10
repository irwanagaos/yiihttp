# yiihttp
Change Display off Http ON Yii 2

UPDATE File : config/web.php IN 'components' array

		'urlManager' => [
		  'showScriptName' => false,
		  'enablePrettyUrl' => true
		],    

ADD file : .htaccess IN folder WEB
		RewriteEngine on
 
		# If a directory or a file exists, use it directly
		RewriteCond %{REQUEST_FILENAME} !-f
		RewriteCond %{REQUEST_FILENAME} !-d
		# Otherwise forward it to index.php
		RewriteRule . index.php
