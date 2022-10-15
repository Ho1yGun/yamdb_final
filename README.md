![yamdb_workflow](https://github.com/Ho1yGun/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)
# yamdb_final

### Проект YaMDb собирает отзывы пользователей на произведения.
### Произведения делятся на категории, такие как «Книги», «Фильмы», «Музыка». Список категорий может быть расширен


## Как запустить проект <img src = "https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue" /> 

### Клонировать репозиторий и перейти в него в командной строке:

```
HTTPS: git clone https://github.com/Ho1yGun/yamdb_final.git
SSH: git clone git@github.com:Ho1yGun/yamdb_final.git
```

### Создайте и заполните файл .env в /infra с переменными окружения для работы с базой данных
```
DB_ENGINE=django.db.backends.postgresql # указываем, что работаем с postgresql
DB_NAME= # укажите имя базы данных
POSTGRES_USER= # логин для подключения к базе данных (установите свой)
POSTGRES_PASSWORD= # пароль для подключения к БД (установите свой)
DB_HOST= # название сервиса (контейнера)
DB_PORT= # порт для подключения к БД 
```

### перейдите в Git->settings->secrets->actions и добавьте следующую секретную информацию
```
DB_ENGINE - указываем, что работаем с postgresql
DB_HOST - название сервиса (контейнера)
DB_NAME - указываем имя базы данных
DB_PORT - порт для подключения к БД
DOCKER_USERNAME
DOCKER_PASSWORD
HOST - ip адрес сервера
PASSPHRASE - фраза_пароль при создании ssh-ключа
POSTGRES_PASSWORD - пароль для подключения к БД (установите свой)
POSTGRES_USER - логин для подключения к базе данных (установите свой)
SSH_KEY - приватный ключ с компьютера, имеющего доступ к серверу
TELEGRAM_TO - ID своего телеграм-аккаунта
TELEGRAM_TOKEN - токен вашего бота
USER - имя пользователя для подключения к серверу
```
### Подготовьте сервер:
#### Остановите службу nginx: 
```
sudo systemctl stop nginx 
```
#### Установите docker:
```
sudo apt install docker.io 
```
#### Установите docker-compose, с этим вам поможет официальная документация.
```
https://docs.docker.com/compose/install/
```
#### Скопируйте файлы docker-compose.yaml и nginx/default.conf из вашего проекта на сервер в home/<ваш_username>/docker-compose.yaml и home/<ваш_username>/nginx/default.conf соответственно.


Автор проекта Ho1yGun. В рамках курса Яндекс.Практикум управление проектом на удалённом сервере.

