# Проект “Сайт рецептов” на Django

Данный проект является реализацией итоговой аттестации по программе “Вебразработка на Python” и представляет собой веб-приложение для хранения и просмотра рецептов. Пользователи могут добавлять, просматривать и редактировать рецепты, а также просматривать рецепты других пользователей.

## Установка
Клонируйте репозиторий на ваше устройство:

git clone [https://github.com/dyaz1337/recipe_site_final_work_python_django]
Установите зависимости:

pip install -r requirements.txt
Создайте базу данных MySQL и настройте соединение с базой данных в файле settings.py:

DATABASES = {
'default': {
    'ENGINE': 'django.db.backends.mysql',
    'NAME': 'dma$default',
    'USER': dma',
    'PASSWORD': os.getenv('MYSQL_PASSWORD'),
    'HOST': 'dma.mysql.pythonanywhere-services.com',
    'OPTIONS': {
        'init_command': "SET NAMES 'utf8mb4';SET sql_mode='STRICT_TRANS_TABLES'",
        'charset': 'utf8mb4',
    },
}
Или можете раскомментировать следующие строки для работы с sqlite3 (и удалить строки ниже до блока # Password validation):

DATABASES = {
  'default': {
      'ENGINE': 'django.db.backends.sqlite3',
      'NAME': BASE_DIR / 'db.sqlite3',
  }
}
Примените миграции базы данных:

python manage.py migrate
Для создания суперпользователя:

python manage.py createsuperuser
Запустите сервер разработки Django:

python manage.py runserver
Откройте ваш веб-браузер и перейдите по адресу http://localhost:8000/, чтобы начать использование приложения.

# Функции
Регистрация и аутентификация пользователей
Просмотр главной страницы с 3 рецептами кратко
Просмотр подробной информации о рецепте
Добавление, редактирование рецептов
Возможность добавления изображения для рецепта
Категоризация рецептов

# Технологии
- Python
- Django - фреймворк для разработки веб-приложений
- MySQL - СУБД для хранения данных
- HTML/CSS - для создания пользовательского интерфейса

  # Сайты
[dma.pythonanywhere.com](https://dma.pythonanywhere.com/)
Google Docs https://docs.google.com/document/d/1-UciHNLhO-qybxnYrKQYBorEaBkzgTmc5K_reYBSxWA/edit?usp=sharing
