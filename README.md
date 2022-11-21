# SWPP Practice Session #10
- Connected frontend and backend
- Deploy

## Docker 
```
docker pull snuspl/swpp:practice8

docker run --rm -it \
    --ipc=host \
    --name "practice10" \
    -p 0.0.0.0:3000:3000 -p 0.0.0.0:8000:8000 \
    -v ${PWD}:/home \
    snuspl/swpp:practice8 \
    /bin/bash
```

## Frontend
```
cd frontend
yarn
yarn start
```

## Backend
```
cd backend
python manage.py makemigrations
python manage.py migrate
python manage.py runserver 0.0.0.0:8000
```