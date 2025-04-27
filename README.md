# Real-Time WebSocket Chat Application

Цей проект реалізує веб-додаток для обміну повідомленнями в реальному часі з використанням WebSocket. Сервер побудований на FastAPI, а клієнт взаємодіє з ним через WebSocket.

## Структура проекту

- **app/main.py** - Основний серверний файл FastAPI.

- **app/websocket_manager.py** - Менеджер для керування WebSocket підключеннями.

- **app/static/index.html** - Фронтенд для взаємодії з сервером через WebSocket.

- **Dockerfile** - Для створення Docker-контейнера.

- **requirements.txt** - Перелік необхідних бібліотек для проекту.

## Як запустити проект

1. Клонуйте репозиторій:
   ```bash
   git clone https://github.com/db-user/vebprogLR9.git
   cd real-time-chat
   ```
2. Створіть і активуйте віртуальне середовище:

```
python -m venv venv
source venv/bin/activate  # для Linux/macOS
venv\Scripts\activate  # для Windows
```
3. Встановіть залежності:

```
pip install -r requirements.txt
```

4. Запустіть сервер:

```
uvicorn app.main:app --reload
```
5. Відкрийте app/static/index.html в браузері, щоб почати використовувати чат.

## Документація
**Основна архітектура:**

Використовується WebSocket для двостороннього зв'язку між сервером і клієнтом.

Клієнт підключається до серверу через ендпоінт /ws.

**Масштабованість:**

Можна масштабувати сервер за допомогою Redis для обміну повідомленнями між кількома інстансами.

## Ліцензія
MIT License
