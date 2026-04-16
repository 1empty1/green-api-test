# Effective Mobile Test Task

Веб-приложение с nginx и Python backend в Docker.

## Как это работает

```
Пользователь → Nginx (порт 80) → Backend (порт 8080)
```

Nginx принимает запросы и проксирует их на Python-сервер. Backend доступен только внутри docker-сети.

## Технологии

- Docker & Docker Compose
- Python 3.11 (http.server)
- Nginx 1.25 (Alpine)

## Запуск

Требования: Docker и Docker Compose

```bash
docker-compose up -d --build
```

## Проверка

```bash
curl http://localhost
```

Должно вернуть: `Hello from Effective Mobile!`

Или просто открой http://localhost в браузере.

## Структура

```
├── backend/
│   ├── Dockerfile
│   └── app.py
├── nginx/
│   └── nginx.conf
├── docker-compose.yml
└── README.md
```

## Остановка

```bash
docker-compose down
```

## Что реализовано

- Backend на Python (http.server) слушает порт 8080
- Nginx проксирует запросы с порта 80
- Контейнеры в отдельной docker-сети
- Backend запускается не от root
- Healthcheck'и для мониторинга состояния
