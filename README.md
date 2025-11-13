# Imp-codes
Important Codes

### Redirect from WWW to Non-WWW
RewriteEngine On
RewriteCond %{HTTP_HOST} ^www\.(.+)$ [NC]
RewriteRule ^(.*)$ https://%1/$1 [R=301,L]


### Redirect from Non-WWW to WWW
RewriteEngine On
RewriteCond %{HTTP_HOST} !^www\. [NC]
RewriteCond %{HTTP_HOST} ^(?!$)(.+)$ [NC]
RewriteRule ^(.*)$ https://www.%1/$1 [R=301,L]
