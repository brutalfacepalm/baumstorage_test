### Запуск приложения
Для запуска приложения достаточно скопировать репозиторий и ввести команды:

    docker compose build
    docker compose up

Документация по-умолчанию доступна по адресу:
    
    0.0.0.0:8888/

Отправка исходных данных:

    0.0.0.0:8888/send_text

Отображение статистики по загруженным(в т.ч. загружаемым) исходным данным:

    0.0.0.0:8888/get_stats

### Параметры приложения
Все основные параметры приложения указываются в файлах _docker-compose.yml_ и _.env.dev_
Например, для задачи числа _workers_ __FastAPI__:
    
    [docker-compose.yml]
    command: python app.py --workers 4
    
Или имя основной базы данных Postgres для работы внутри приложения:
    
    [.env.dev]
    DATABASE_NAME=fastapi

### Тестовый запуск
Чтобы проверить работу приложения можно запустить код из модуля:
    
    python load_test_data.py

Отследить процесс работы приложения возможно или запросив статистику(__0.0.0.0:8888/get_stats__)
Или в __GUI pgAdmin(0.0.0.0:5050)__
    


