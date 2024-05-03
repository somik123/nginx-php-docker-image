# nginx-php-docker-image

## How to use
Pull docker image: 
```
docker image pull somik123/php-nginx:latest
```

Place your php files in a folder accessible by docker or the user running the files. Example:
`/home/somik/html`

Start the container with the command:
```
docker run -p 8080:80 -dt -v /home/somik/html:/var/www/html --name nginx-php somik123/nginx-php
```

Note that this will run the container with port `8080` on host mapped to the container's nginx running on port `80`.