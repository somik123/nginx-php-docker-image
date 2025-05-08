# nginx-php-docker-image

## How to use (with docker-compose)
1. Copy the `docker-compose.yml` to a folder of your choice.
1. Edit the file and change the container name.
1. Create a html folder in the same directory as the `docker-compose.yml` file and place your php/css/js and other files in there.
1. Start the container with the following command:
   ```
   docker compose up -d
   ```


## How to use (with docker command)
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