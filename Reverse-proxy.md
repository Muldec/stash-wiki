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