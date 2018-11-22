# Display API documentation

Display API documentation in a Express application usin swagger UI

## Installation and launch

Clone the projet
Move to "api-doc-edition" folder
Install dependencies

  > git clone ...
  > cd api-doc-edition
  > npm i

Launch the server

  > npm start

## Deploy it in prod

### Prerequist

Node and NPM should be installed in your server

### Deploy it 

clone the project using git in $REPO of your choise

  > git clone https://github.com/kolok/myits-swagger.git

Configure systemd to launch your node application as it is explain in this blog:
[https://nodesource.com/blog/running-your-node-js-app-with-systemd-part-1/](https://nodesource.com/blog/running-your-node-js-app-with-systemd-part-1/)

Enable apache module proxy and proxy_http

Add proxy configuration, For example :

  ProxyPass "/api-docs" "http://localhost:3002/api-docs"
  ProxyPassReverse "/api-docs" "http://localhost:3002/api-docs"

## Useful links

I was mainly inspired and I copied a lot from : [https://github.com/GenFirst/swagger-to-existing-nodejs-project](https://github.com/GenFirst/swagger-to-existing-nodejs-project)
About node + systemd : [https://nodesource.com/blog/running-your-node-js-app-with-systemd-part-1/](https://nodesource.com/blog/running-your-node-js-app-with-systemd-part-1/)

