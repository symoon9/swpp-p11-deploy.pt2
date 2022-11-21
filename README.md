# SWPP Practice Session #10
- Connected frontend and backend
- Deploy

## Docker 
We provide a docker image that contains `django`, `uwsgi`, and `nginx`.
```
docker pull snuspl/swpp:practice11
```

Build backend docker image by 
```
cd backend
sudo docker build -t backend .
```

Build frontend docker image by 
```
cd frontend
sudo docker build -t frontend .
```

## Frontend
```
sudo docker run -d --rm\
    --name "frontend" \
    -p 80:80 \
    frontend:latest
```

## Backend
```
sudo docker run -d --rm\
    --name "backend" \
    -p 8000:8000 \
    backend:latest 
```