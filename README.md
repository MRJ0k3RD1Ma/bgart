# bgart
OOO Beautiful Perfect Grand firmasi uchun loyiha

# a.bgart.local
    <VirtualHost *:80>
        ServerName a.bgart.local
        DocumentRoot "path/to/bgart/bgadmin/web"
        
        <Directory "path/to/bgart/bgadmin/web">
            RewriteEngine on
            RewriteCond %{REQUEST_FILENAME} !-f
            RewriteCond %{REQUEST_FILENAME} !-d
            RewriteRule . index.php
			DirectoryIndex index.php
			Require all granted
		</Directory>
    </VirtualHost>


# r.bgart.local
    <VirtualHost *:80>
        ServerName r.bgart.local
        DocumentRoot "path/to/bgart/yatt/web"
        <Directory "path/to/bgart/yatt/web">
            RewriteEngine on
            RewriteCond %{REQUEST_FILENAME} !-f
            RewriteCond %{REQUEST_FILENAME} !-d
            RewriteRule . index.php
			DirectoryIndex index.php
			Require all granted
		</Directory>
    </VirtualHost>

# t.bgart.local

    <VirtualHost *:80>
        ServerName t.bgart.local
        DocumentRoot "path/to/bgart/distributor/web"
        <Directory "path/to/bgart/distributor/web">
            RewriteEngine on
            RewriteCond %{REQUEST_FILENAME} !-f
            RewriteCond %{REQUEST_FILENAME} !-d
            RewriteRule . index.php
            DirectoryIndex index.php
            Require all granted
        </Directory>
    </VirtualHost>
