# profile
<h1 align="center">I'm Tai. I'm crazy.</h1>
<h3 align="left"> I love studing English language </h3>
<h3 align="left"> Language and Tools: </h3>

\
By default, the Docker will expose port 8080, so change this within the\
Dockerfile if necessary. When ready, simply use the Dockerfile to\
build the image.\
\
```sh\
cd dillinger\
docker build -t <youruser>/dillinger:$\{package.json.version\} .\
```\
\
This will create the dillinger image and pull in the necessary dependencies.\
Be sure to swap out $\{package.json.version\} with the actual\
version of Dillinger.\
\
Once done, run the Docker image and map the port to whatever you wish on\
your host. In this example, we simply map port 8000 of the host to\
port 8080 of the Docker (or whatever port was exposed in the Dockerfile):\
```sh\
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:$\{package.json.version\}\
```\
\
> Note: --capt-add=SYS-ADMIN is required for PDF rendering.\
\
Verify the deployment by navigating to your server address in\
your preferred browser.\
\
```sh\
127.0.0.1:8000\
```\
}
