# mTLS-server-client
This repository has a simpler server/client go code and a Dockerfile for building the app

Reference:
1. How to build mTLS based client server
https://venilnoronha.io/a-step-by-step-guide-to-mtls-in-go

2. How to build a go app into a docker image
https://www.callicoder.com/docker-golang-image-container-example/

3. To run the client, build the go binary and execute it or use
`go run client.go` command

4. The certs I generated are for my server domain, replace the cert generation
command with the server's IP/FQDN and replace here:
```
openssl req -newkey rsa:2048 \
  -new -nodes -x509 \
  -days 3650 \
  -out cert.pem \
  -keyout key.pem \
  -subj "/C=US/ST=California/L=Mountain View/O=Your Organization/OU=Your Unit/CN=<server IP/FQDN>"
  ```
