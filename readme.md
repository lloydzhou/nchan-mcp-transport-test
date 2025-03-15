
1. run nchan transport

```
sudo docker run --rm -it -v `pwd`/nchan.conf:/etc/nginx/conf.d/nchan.conf -p 8888:80 lloydzhou/nchan
```

2. test with curl

```
curl -H "Accept:text/event-stream" localhost:8888/mcp/testname/test_session_id

: hi

event: endpoint
id: 1742013694:0
data: /mcp/testname/test_session_id

...
```

3. run inspector
> the old version can not connect success
```
npx -y @modelcontextprotocol/inspector
```

> the new version with Accept header
```
build inspector

node ./bin/cli.js

```

![Image](https://github.com/user-attachments/assets/9161ca1b-94e7-4150-8b9d-953c893b40d4)

