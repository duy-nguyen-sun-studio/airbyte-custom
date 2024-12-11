Step to update facebook ads custom connector:

- cd to airbyte repository root directory

- Install to local docker repository using command: 
```
airbyte-ci connectors --name=source-facebook-marketing build --architecture=linux/amd64
```

- Login to docker
```
docker login -u duynguyen2509
<PERSONAL_ACCESS_TOKEN>
```

- Tag using command:
```
docker tag airbyte/source-facebook-marketing:dev duynguyen2509/source-facebook-marketing-custom:1.0.0
```

- Push to online docker repository using command:
```
docker push duynguyen2509/source-facebook-marketing-custom:1.0.0
```

- SSH to airbyte instance and login using command:
```
sudo docker login -u duynguyen2509
<PERSONAL_ACCESS_TOKEN>
```

- Pull image using command:
```
sudo docker pull duynguyen2509/source-facebook-marketing-custom:1.0.0
```

- Setup new connector:
display name: Facebook Marketing Custom
repository name: duynguyen2509/source-facebook-marketing-custom
image tag: 1.0.0