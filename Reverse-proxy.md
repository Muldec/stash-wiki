The use of nginx as a reverse proxy for stash is possible. 
A sample configuration of headers that need to be set mentioned [here](https://github.com/stashapp/stash/pull/134) is 
```
location / {
    proxy_pass http://127.0.0.1:9999;
    proxy_set_header Host $host;
    proxy_set_header X-Real-IP $remote_addr;
    proxy_set_header X-Forwarded-For $remote_addr;
    proxy_set_header X-Forwarded-Port $server_port;
    proxy_set_header X-Forwarded-Proto $scheme;
}
```
As of commit **7767271**, if needed you can adjust the **external_host** setting to your external address as mentioned [here](https://github.com/stashapp/stash/pull/369)

In order for the websocket to work, you may need to also add these lines to your server block (`proxy.conf` file in the Letencrypt Unraid docker container for instance) as mentioned [here](https://github.com/stashapp/stash/issues/532)

```
proxy_http_version 1.1;
proxy_set_header Upgrade $http_upgrade;
proxy_set_header Connection "upgrade";
```