# PexFroge-App
Hoofdrepo voor het project PexFroge

# Initial setup

## Linux/ Mac
clone de repository ergens op je local machine en open de directory in je terminal.
```
git clone https://github.com/koelekikkersklub/PexFroge-App
cd PexFroge-App
git submodule init
git submodule update
```

copy example env file
```
cp .env.example .env
```


install composer so it doesn't need to be run on the host
```
docker run --rm -v $(pwd)/laravel:/app composer install
```

start de stack en generate application key
```
docker compose up -d
docker compose exec app php artisan key:generate
```
## Windows

clone de repository ergens op je local machine en open de directory in je terminal.
```
git clone https://github.com/koelekikkersklub/PexFroge-App
cd PexFroge-App
git submodule init
git submodule update
```

copy example env file
```
copy .env.example .env
```

install composer so it doesn't need to be run on the host
```
docker run --rm -v $(pwd)/laravel:/app composer install
```

start de stack en generate application key
```
docker compose up -d
docker compose exec app php artisan key:generate
```


# Running the stack for development
```
cd PexFroge-App
docker compose up -d
```

# Shutting down the stack
```
docker compose down
```

# Making changes to the laravel submodule
When your working directory is within the laravel submodule, the tracked repo automatically refers to https://github.com/KoeleKikkersKlub/PexFroge-laravel.
You commit changes to this repo as normal when using the command line, and if you're using a gui it will most likely be shown as a separate tracked repo where you commit to as normal as well.
