# Fastify

- You want to manage two versions of a RESTful Web Service country API with fastify.
Complete the following code snippet in a way that fastify route prefixing is used for the two API versions v1 and v2.
Version v1 of the API is saved in file routes/v1/country.js, and version v2 in file routes/v2/country.js.
The server should listen to port 5500.
You are not allowed to add any additional lines!

    ```js
    // this is file server.js
    
    const fastify = require("fastify")
    
    fastify.register(require("routes/v1/country.js"), {prefix: "/v1"})
    fastify.register(require("routes/v2/country.js"), {prefix: "/v2"})
    
    fastify.listen(5500)
    ```