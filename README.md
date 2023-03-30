----------------------------------------------------------------------------------------------------------------------
> Задание выполнено студентом ```Leonids Jofe``` из школы SkillFactory, курс Full-stack python developer, поток ```FPW-104```
----------------------------------------------------------------------------------------------------------------------

Вам понадобится ↓
```
pip install django
pip install django-allauth
pip install django-apscheduler
pip install django-filter
pip install redis
pip install celery
```

Отчет о работе ↓
- Установить Redis. +
- Установить Celery. +

- Произвести необходимые конфигурации Django для соединения всех компонент системы. ↓ +
- 1. \D7\NewsPortal\Engine\celery.py
- 2. \D7\NewsPortal\Engine\\__init__.py
- 3. \D7\NewsPortal\Engine\settings.py

- Реализовать рассылку уведомлений подписчикам после создания новости. ↓ +
- 1. \D7\NewsPortal\Posts\views.py Запуск
- 2. \D7\NewsPortal\Cron\tasks.py Мозг
- 3. Запуск ```python manage.py runserver```
- 4. Запуск ```celery -A Engine worker -l INFO --pool=solo```

- Реализовать еженедельную рассылку с последними новостями (каждый понедельник в 8:00 утра). ↓ +
- 1. \D7\NewsPortal\Engine\celery.py Запуск
- 2. \D7\NewsPortal\Cron\tasks.py Мозг
- 3. Запуск ```python manage.py runserver```
- 4. Запуск ```celery -A Engine worker -l INFO --pool=solo```
- 5. Запуск ```celery -A Engine beat -l INFO```
