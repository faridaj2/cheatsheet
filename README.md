# 1. File .htaccess
RewriteCond %{REQUEST_FILENAME} !-d  
RewriteCond %{REQUEST_FILENAME} !-f  
RewriteRule ^ index.php [L]

# 2. file index.php 
$app->bind('path.public', function() {  
    return `__DIR__`;  
});
