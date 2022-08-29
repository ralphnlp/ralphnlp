# profile
<h1 align="center">I'm Tai. I'm crazy.</h1>
<h3 align="left"> I love studing English language </h3>
<h3 align="left"> Language and Tools: </h3>
<p align="left"> <a href="https://www.cprogramming.com/" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="c" width="40" height="40"/> </a> <a href="https://www.w3schools.com/css/" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://www.docker.com/" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="docker" width="40" height="40"/> </a> <a href="https://www.w3.org/html/" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a> <a href="https://www.adobe.com/in/products/illustrator.html" target="_blank"> <img src="https://www.vectorlogo.zone/logos/adobe_illustrator/adobe_illustrator-icon.svg" alt="illustrator" width="40" height="40"/> </a> <a href="https://www.java.com" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="java" width="40" height="40"/> </a> <a href="https://www.mathworks.com/" target="_blank"> <img src="https://upload.wikimedia.org/wikipedia/commons/2/21/Matlab_Logo.png" alt="matlab" width="40" height="40"/> </a> <a href="https://opencv.org/" target="_blank"> <img src="https://www.vectorlogo.zone/logos/opencv/opencv-icon.svg" alt="opencv" width="40" height="40"/> </a> <a href="https://www.photoshop.com/en" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/photoshop/photoshop-line.svg" alt="photoshop" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://www.tensorflow.org" target="_blank"> <img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" alt="tensorflow" width="40" height="40"/> </a> </p>
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
