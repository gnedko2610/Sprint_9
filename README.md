# Sprint_9
Автотесты на Selenium для сервиса «Продуктовый помощник» (Foodgram).

## Структура

assets/
    test_image.jpg
pages/
    __init__.py
    base_page.py
    main_page.py
    login_page.py
    register_page.py
    create_recipe_page.py
locators/
    __init__.py
    main_page_locators.py
    login_page_locators.py
    register_page_locators.py
    create_recipe_page_locators.py
tests/
    test_register.py
    test_login.py
    test_create_recipe.py
helpers/
    helpers.py
data/
    test_data.py
conftest.py
constants.py
Dockerfile
docker-compose.yml
browser.json
.github/
    workflows/
        ci.yml

## Запуск тестов

### Локально (с Chrome)
pytest -v

### Через Selenoid + Docker Compose
bash
docker pull selenoid/chrome:128.0
docker-compose up --build

### Генерация Allure отчёта
Команда для генерации Allure-отчёта:
pytest --alluredir=allure_results
Команда для формирования отчёта в формате веб-страницы:
allure serve allure_results