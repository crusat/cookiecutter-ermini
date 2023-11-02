## Start of configuration add by letsencrypt container
location ^~ /.well-known/acme-challenge/ {
    auth_basic off;
    auth_request off;
    allow all;
    root /usr/share/nginx/html;
    try_files $uri =404;
    break;
}
## End of configuration add by letsencrypt container
server_tokens off;
client_max_body_size 2000m;

#client_max_body_size 100M;
proxy_connect_timeout 3000;
proxy_send_timeout 3000;
proxy_read_timeout 3000;
send_timeout 3000;
