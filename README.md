# GREEN-API Test Interface

Тестовое задание на должность DevOps разработчик.

HTML-страница для тестирования методов GREEN-API (WhatsApp API).

## Описание

Веб-интерфейс для работы с GREEN-API, позволяющий:
- Получать настройки инстанса (getSettings)
- Проверять состояние инстанса (getStateInstance)
- Отправлять текстовые сообщения (sendMessage)
- Отправлять файлы по URL (sendFileByUrl)

## Технологии

- HTML5
- CSS3
- JavaScript (Vanilla JS)
- GREEN-API REST API

## Установка и запуск

1. Клонировать репозиторий:
```bash
git clone https://github.com/YOUR_USERNAME/green-api-test.git
cd green-api-test
```

2. Открыть `index.html` в браузере

Или запустить локальный сервер:
```bash
python -m http.server 8000
```

Затем открыть: http://localhost:8000

## Использование

1. Зарегистрироваться на https://console.green-api.com/
2. Создать новый инстанс (бесплатный тариф Developer)
3. Отсканировать QR-код для авторизации WhatsApp
4. Скопировать `idInstance` и `apiTokenInstance`
5. Вставить учетные данные на странице
6. Нажать кнопки для тестирования методов API

### Формат chatId

- Личный чат: `7xxxxxxxxxx@c.us`
- Групповой чат: `7xxxxxxxxxx-xxxxxxxxxx@g.us`

## Структура проекта

```
.
├── index.html          # Основной файл приложения
└── README.md          # Документация
```

## API Endpoints

- `GET /waInstance{idInstance}/getSettings/{apiTokenInstance}`
- `GET /waInstance{idInstance}/getStateInstance/{apiTokenInstance}`
- `POST /waInstance{idInstance}/sendMessage/{apiTokenInstance}`
- `POST /waInstance{idInstance}/sendFileByUrl/{apiTokenInstance}`

## Документация GREEN-API

- [Официальная документация](https://green-api.com/docs/api/)
- [GetSettings](https://green-api.com/docs/api/account/GetSettings/)
- [GetStateInstance](https://green-api.com/docs/api/account/GetStateInstance/)
- [SendMessage](https://green-api.com/docs/api/sending/SendMessage/)
- [SendFileByUrl](https://green-api.com/docs/api/sending/SendFileByUrl/)

## Автор

1empty1

## Лицензия

MIT
