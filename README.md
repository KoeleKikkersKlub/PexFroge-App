# PexFroge-App
Hoofdrepo voor het project PexFroge

# Initial setup
clone de repository ergens op je local machine en open de directiry in je terminal.
```
git clone https://github.com/koelekikkersklub/PexFroge-App
cd PexFroge-App
git submodule init
git submodule update
```

copy example env file
```
cp .env.example .env
if using windows, use:
copy .env.example .env
```


install composer so it doesn't need to be run on the host
```
docker run --rm -v $(pwd)/laravel:/app composer install
if using windows, use:
docker run --rm -v "%cd%\laravel:/app" composer install
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
