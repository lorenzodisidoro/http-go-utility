# http-go-utility

http-go-utility is utility GO package for making HTTP calls

## Install package

```sh
go get github.com/vulpemventures/http-go-utility
```

## Public methods

```go
Request(method string, url string, bodyString string, header map[string]string) (string, error)
```

## Example
Import package
```go
import utilhttp "github.com/vulpemventures/http-go-utility"
```

and use like that
```go
method := "GET"
url := "https://api.blockcypher.com/v1/btc/test3/addrs/mtXWDB6k5yC5v7TcwKZHB89SUp85yCKshy?unspentOnly=true"
response, err := utilhttp.Request(method, url, "", nil)
if err != nil {
  fmt.Println("An error occurred:", err)
  return
}

fmt.Println("Response:", response)
```