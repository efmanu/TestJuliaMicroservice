# Julia Microservice Example
Sample Microservice with Julia

### Run Microservice
From root folder of this project
```
julia --project
```
#### Instantiate (Do once)
```julia
using Pkg
Pkg.instantiate()
```

#### Start Server

```julia
using TestJuliaMicroservice
TestJuliaMicroservice.run()
```

Default server will run in `localhost` with `3000` port

You can test by hitting `localhost:3000/api/live` in browser. You wil get response as `OK`.

Also you can test a post request to calculate the square of a number as below in terminal \command line.
```
curl -XPOST -H "Content-type: application/json" -d '{
     "number" : 2
}' 'http://localhost:3000/api/find_square_req'
```

You will get response as below:

```
{"number":2,"square":4}
```


