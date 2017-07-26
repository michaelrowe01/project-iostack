# Install golang (https://golang.org/dl/)

```sh
# ex for v1.8.3/linux amd64:
wget "https://storage.googleapis.com/golang/go1.8.3.linux-amd64.tar.gz"

# extract go.tar.gz in /usr/local folder
tar -C /usr/local -xzf go1.8.3.linux-amd64.tar.gz

# export variable to access go from everywhere
export PATH=$PATH:/usr/local/go/bin

# remove tar.gz file
rm go1.8.3.linux-amd64.tar.gz
```

# Check working

```sh
mkdir gotest/

echo 'package main' > gotest/gotest.go
echo 'import "fmt"' >> gotest/gotest.go
echo 'func main() {' >> gotest/gotest.go
echo '   fmt.Printf("Hello world !\n")' >> gotest/gotest.go
echo '}' >> gotest/gotest.go

cd gotest
go build
./gotest

# should print 'Hello world !'
```