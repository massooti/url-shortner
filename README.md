<h1>URL Shortener App</h1>
This is a simple URL shortener app written in Go. The app uses Redis as the database for storing and retrieving links.

### Installation
To install the app, you will need to have Go and Redis installed on your system.

1- Clone the repository to your local machine:

```
git clone https://github.com/massooti/url-shortener.git

```

2- Install the dependencies:

```
go get github.com/go-redis/redis

```

3-Start Redis server:
```
redis-server

```

4- Run the app:

```
go run main.go
```

5 - Access the app in your browser at ```http://localhost:8080```

### Usage
To use the app, simply enter a long URL into the input field and click "Shorten". The app will generate a short URL that can be used to redirect to the original URL.


#### API
The app also includes an API for generating short URLs programmatically. The API has a single endpoint:
POST /api/shorten
* Request Parameters:

```url (required): The long URL to be shortened.```
* Response:

```short_url: The generated short URL.```

### Example

```
curl -X POST -d '{"url": "https://www.google.com"}' http://localhost:8080/api/shorten
```

```
{
  "short_url": "http://localhost:8080/d4a32f"
}

```

### Configuration
The app can be configured using environment variables. The following variables are available:

* REDIS_ADDR: The address of the Redis server (default: localhost:6379)
* PORT: The port number to run the app on (default: 8080)


### TODO

1- make the app dockerize
