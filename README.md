# Restful Assessment

##### Run with docker

```git remote add origin https://github.com/arafatr234/restful_assesment.git
```
Move to root of project and execute,
```
docker build -t repository_name:tag_name .
```
then run docker,
```
docker run -p 8080:4567 repository_name:tag_name
```

Or get it from docker hub,
```
docker pull arafatr234/restful_assessment:2.7
docker run -p 8080:4567 arafatr234/restful_assessment:2.7
```

##### Run with jar

Install java in your system
[Download JAR from here](https://github.com/arafatr234/restful_assessment/releases/download/1.3/restful_assessment-1.3.jar)

then execute 

```
java -jar downloadfile.jar
```

## Documentation

Application port docker `8080` and JAR `4567`

BASE_URL : `host_name:$port`

1. Get Values : 

GET /values
```json
{
    "key1": "value1",
    "key2": "value2"
    .....
}
```
or

GET /values?keys=key1,key3
```json
{
    "key1": "value1",
    "key3": "value3"
    .....
}
```

2. Add Values

POST /values

Request,
```json
{
    "key1": "value1",
    "key2": "value2"
}
```

Response,
```
{
    "code": 200
}
```
or
```
{
    "code": 201
}
```

Note : MongoDB used to store data & Redis used for data caching. In get request result will be cached for 10seconds.
