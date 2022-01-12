# nomad-demo

## setup

- set registry
```
docker pull registry
docker run -d -p 5000:5000 registry
```

- check  
<http://localhost:5000/v2/_catalog>

- install nomad

```
brew install nomad
nomad -v
```

- start nomad

``` 
nomad agent -config server.hcl
nomad agent -config client1.hcl
nomad agent -config client2.hcl
```

- set permission

```
cd /tmp
chmod -R 755 server1
chmod -R 755 client1
chmod -R 755 client2
```

- check  
<http://localhost:4646/ui/jobs>
