```
docker run -d -p 27017:27017 --name mongo mongo

docker run -d                                \
             -e APP_ID=sishu         \
             -e MASTER_KEY=sishu2018key \
             -p 1337:1337                      \
             --link mongo                      \
             --name parse-server               \
             yongjhih/parse-server




curl -X POST \
  -H "X-Parse-Application-Id: sishu" \
  -H "Content-Type: application/json" \
  -d '{}' \
  http://192.168.99.100:1337/parse/functions/hello





  docker run -d \
        -e PARSE_DASHBOARD_CONFIG='{"apps":[{"appId":"demo","serverURL":"http://47.93.192.198:1337/parse","masterKey":"demolijianfei","appName":"demo"}],"users":[{"user":"admin","pass":"demolijianfei"}]}' \
        -e PARSE_DASHBOARD_ALLOW_INSECURE_HTTP=1  \
        -p 4040:4040                      \
        --link parse-server               \
        --name parse-dashboard            \
        yongjhih/parse-dashboard



docker run -d                                \
             -e APP_ID=demo         \
             -e MASTER_KEY=demolijianfei \
             -p 1337:1337                      \
             --link mongo                      \
             --name parse-server               \
             parseplatform/parse-server



  docker run -d \
        -e PARSE_DASHBOARD_CONFIG='{"apps":[{"appId":"sishu","serverURL":"http://parseserver.sishuxuefu.com/parse","masterKey":"sishu2018key","appName":"sishu"}],"users":[{"user":"admin","pass":"sishu725"}]}' \
        -e PARSE_DASHBOARD_ALLOW_INSECURE_HTTP=1  \
        -p 4040:4040                      \
        --link parse-server               \
        --name parse-dashboard            \
        parseplatform/parse-dashboard
```

