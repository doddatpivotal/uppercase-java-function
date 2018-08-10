to add to riff

```bash
riff function create java uppercase --git-repo https://github.com/doddatpivotal/uppercase-java-function.git --artifact target/demo-0.0.1-SNAPSHOT.jar --image gcr.io/$GCP_PROJECT/uppercase-node-function --handler "uppercase&main=com.example.demo.DemoApplication"
```

to test
```bash
curl      -w '\n'      -H 'Host: uppercase.default.example.com'           http://$SERVICE_IP      -d hello
```

to delete

```bash
riff service delete uppercase
```

current error response
```bash
[]{"timestamp":"Aug 10, 2018 7:26:11 PM","status":200,"error":"OK","exception":"java.lang.ClassCastException","message":"org.springframework.util.LinkedMultiValueMap cannot be cast to java.lang.String","path":"/"}
```