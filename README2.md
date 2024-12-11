Step to update facebook ads custom connector:

- cd to airbyte repository root directory

- Install to local docker repository using command: 
```
airbyte-ci connectors --name=source-facebook-marketing build
```

- Login to docker
```
docker login -u duynguyen2509
<PERSONAL_ACCESS_TOKEN>
```

- Tag using command:
```
docker tag airbyte/source-facebook-marketing:dev duynguyen2509/airbyte:fbads
```

- Push to online docker repository using command:
```
docker push duynguyen2509/airbyte:fbads
```