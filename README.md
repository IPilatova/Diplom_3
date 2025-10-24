## Diplom_3

### Проект автоматизации UI-тестирования программы, которая помогает заказать бургер в Stellar Burgers
- Сервис заказа бургеров - [Stellar Burgers](https://stellarburgers.nomoreparties.site/)
- Документация API - [API Stella Burgers](https://code.s3.yandex.net/qa-automation-engineer/python-full/diploma/api-documentation.pdf)

### Структура проекта
- `locators` - пакет, содержащий локаторы, разделенные по функционалам
- `pages` - пакет, содержащий объекты страниц
- `tests` - пакет, содержащий тесты, разделенные по классам
- `utils` - пакет, содержащий вспомогательные методы и данные (генерация данных, тестовые данные, url страниц)
- `config` - пакет, содержащий базовый url и эндпоинты страниц для вспомогательных api методов
- `tmp/allure_report` - отчет Allure


### Установить зависимости 
``` shell
pip3 install -r requirements.txt
```
### Запуск всех тестов с отчетом Allure
```shell
pytest -v --alluredir=tmp/allure_results
```
### Открытие отчета Allure
```shell
allure serve tmp/allure_results
```
### Удаление отчета Allure и запуск тестов с отчетом заново
```shell
rm -r tmp/allure_results; pytest -v --alluredir=tmp/allure_results
```