

# curl test


## 1) health check

```sh

$ curl http://localhost:8082/health

```




## 1) set


```sh
curl -X POST http://localhost:8082/person \
  -H "Content-Type: application/json" \
  -d '{  
  "id": "aaaa",
  "name": "song",
  "age": 20,
  "createdAt": "2022-07-03T01:03:00"
}'

curl -X POST http://localhost:8082/person \
  -H "Content-Type: application/json" \
  -d '{  
  "id": "bbbb",
  "name": "Park",
  "age": 20,
  "createdAt": "2022-07-03T01:03:00"
}'
```



## 2) get

```sh

curl localhost:8082/person/aaaa

curl localhost:8082/person/bbbb


# 1초에 한번씩
while true; do curl localhost:8082/person/aaaa; echo ; sleep 1; done;


```


## 3) delete

```sh
curl -X DELETE localhost:8082/person/aaaa

curl -X DELETE localhost:8082/person/bbbb


```




