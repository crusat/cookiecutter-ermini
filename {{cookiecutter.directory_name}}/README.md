## Разработка

```bash
cp example.env .env
docker compose up -d
python3 -m venv venv
source venv/bin/activate
pip3 install -r requirements.txt
```

## Развертывание

```bash
# Сайт один на сервере
docker compose -f docker-compose-production.yml -f docker-compose-proxy.yml build
docker compose -f docker-compose-production.yml -f docker-compose-proxy.yml up -d

# Много сайтов на сервере
docker compose -f docker-compose-production.yml build
docker compose -f docker-compose-production.yml up -d
```