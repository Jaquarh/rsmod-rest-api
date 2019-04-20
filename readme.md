# Setting up your REST API service

Navigate to your build.gradle and add the following lines into your depdendencies.

```koltin
compile 'com.sparkjava:spark-core:2.3'
testCompile group: 'junit', name: 'junit', version: '4.+'
```

Inside of your game.example.yml, or game.yml for local deployment, add the following to your services.

```koltin
  - class: gg.rsmod.plugins.service.restapi.RestApiService
    origin: "*"
    methods: "GET, POST"
    headers: "X-PINGOTHER, Content-Type"
    auth: false
```

You can modify the configuration of your service here.

- Origin: The IPv4 addresses that CORS is enabled for
- Methods: The HTTP methods that CORS is enabled for
- Headers: The HTTP headers that CORS is enabled for
- Auth: Still in beta, however, future revisions will allow for oAuth to be used

Finally, copy the service direcotry to your plugin services directory.

# Creating your own routes and controllers

// todo

# Your API will run on http://127.0.0.1:4567
