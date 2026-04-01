# Final Exam

> Final exam for checking student knowledge and practical skills


## Test 22: Event-Driven Architecture with RabbitMQ

### Завдання
Продемонструвати розуміння Event-Driven архітектури. Налаштувати базову конфігурацію сервісу RabbitMQ, розгорнути два веб-сервіси на HTML/JS для обміну динамічними повідомленнями в реальному часі. Продемонструвати крос-протокольну взаємодію між браузерними клієнтами та Postman, використовуючи Typescript.

### Структура проекту

```
├── src
│   ├── web1
│   │   └── index.html
│   ├── web2
│   │   └── index.html
├── rabbitmq.conf
├── docker-compose.yml
├── .editorconfig
├── .gitignore
├── package.json
├── README.md
```

### Покрокова інструкція запуску та тестування

1. **Встановіть Docker** (якщо ще не встановлено):
   - [Завантажити Docker Desktop](https://www.docker.com/products/docker-desktop/)

2. **Запустіть RabbitMQ через Docker**:
   - Відкрийте термінал у корені проекту (де знаходиться файл `docker-compose.yml`).
   - Виконайте команду:
     ```
     npm run start:docker
     ```
   - Переконайтесь, що RabbitMQ доступний на http://localhost:15672 (логін: user, пароль: password).

3. **Запустіть локальний сервер для web1 та web2**:
   - Відкрийте папки `src/web1` і `src/web2` у VS Code або іншому редакторі.
   - Запустіть обидва файли `index.html` через Live Server або інший локальний сервер (наприклад, розширення Live Server для VS Code).

4. **Тестування обміну повідомленнями**:
   - Відкрийте обидва клієнти у різних вкладках браузера.
   - Надішліть повідомлення з одного клієнта — воно має зʼявитися у обох вікнах.

5. **Тестування через Postman**:
   - Відкрийте Postman.
   - Створіть новий WebSocket-запит до `ws://localhost:15675/ws`.
   - Надішліть повідомлення у топік `chat` (див. вкладку "Messages" у Postman).
   - Перевірте, що повідомлення зʼявляється у web1 та web2.

6. **Зупинка RabbitMQ**:
   - У терміналі виконайте:
     ```
     npm run stop:docker
     ```

### Примітки
- Для роботи WebSocket потрібен плагін rabbitmq_web_mqtt (вже увімкнено у docker-compose).
- Конфігурація RabbitMQ у файлі `rabbitmq.conf`.
- Якщо порт 15675 зайнятий, змініть його у конфігурації та у клієнтах.

## Test 22:

### Directory Structure
> Продемонструвати розуміння Event-Driven архітектури. А саме налаштувати базової конфігурацію сервісу  RabbitMQ, розгорнувши два веб-сервіси на HTML/JS для обміну динамічними повідомленнями в реальному часі. Продемонстровано успішну крос-протокольну взаємодію між браузерними клієнтами та Postman, використовуючи мову програмування Typescript. Відповідно до структури наведеної нище.

```
├── exam
│   ├── src
│   │   ├── web1 
│   │   │   ├── index.html
│   │   ├── web2 
│   │   │   ├── index.html  
│   ├── <mqtt>.conf  
│   ├── docker-compose.yml
│   ├── .editorconfig
│   ├── .gitignore
│   ├── package.json
│   ├── README.md
└──

```

## Test 22:

### Directory Structure
> Продемонструвати розуміння Event-Driven архітектури. А саме налаштувати базової конфігурацію сервісу  ActiveMQ, розгорнувши два веб-сервіси на HTML/JS для обміну динамічними повідомленнями в реальному часі. Продемонстровано успішну крос-протокольну взаємодію між браузерними клієнтами та Postman, використовуючи мову програмування Typescript. Відповідно до структури наведеної нище.

```
├── exam
│   ├── src
│   │   ├── web1 
│   │   │   ├── index.html
│   │   ├── web2 
│   │   │   ├── index.html  
│   ├── <mqtt>.conf  
│   ├── docker-compose.yml
│   ├── .editorconfig
│   ├── .gitignore
│   ├── package.json
│   ├── README.md
└──

```
