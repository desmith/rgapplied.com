server {
  listen 80;
  listen 443;

  ssl_certificate /opt/code/rgapplied.com/config/nginx/certs/rgapplied-local.crt;
  ssl_certificate_key /opt/code/rgapplied.com/config/nginx/certs/rgapplied-local.key;

  server_name
    rgstatic.com
  ;

  root /opt/code/rgstatic.com/static;

  location / {
    autoindex on;
  }

  # what to serve if upstream is not available or crashes
  error_page 404 500 502 503 504 /error.html;

  access_log /opt/code/rgstatic.com/logs/nginx-access.log;
  error_log /opt/code/rgstatic.com/logs/nginx-error.log;

}

