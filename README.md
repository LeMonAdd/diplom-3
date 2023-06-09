# Дипломный проект № 3. Яндекс практикум, автоматизация Java UI тест

### Используемые технологии

1. Java 11 
2. Junit 4.13.2 
3. Gson 2.10.1 
4. Rest-assured 4.4.0
5. Javafaker 1.0.2 
6. allure-junit4 2.15.0 
7. Allure-rest-assured 2.15.0 
8. Commons-lang3 3.11
9. Selenide 6.13.0
10. Selenium-manager 4.8.3
11. Selenium-java 4.8.3

Тестируемый сервис - https://stellarburgers.nomoreparties.site/

Документация API - https://code.s3.yandex.net/qa-automation-engineer/java/cheatsheets/paid-track/diplom/api-documentation.pdf


### Описание проекта 

Проект может быть запущен в двух браузерах:
1. Chrome - дефолтный браузер реализуемый через Selenide
2. Yandex - для использования данного браузера необходимо в классе BaseTest полю **isYandex** проставить значение true

Веб драйвер для Яндекса хранится по пути src.main.resources.yandexdriver.exe

Проект тестирует **UI составляющую сервиса** https://stellarburgers.nomoreparties.site/ 

В пакете *main.java.base* содержатся классы

*BasePage* - содержит общие для всех страниц методы
*Const* - содержит класс с урлами
*LocalStorageSelenium* - содержит методы работы с локальным хранилищем

В пакете *main.java.model* содержится каркас пользователя и персональные данные

В пакете *main.java.pages* реализован паттерн Page Object

Страницы и элементы страниц разбиты на классы

В проекте используется **параметризация Junit 4** реализованная в классе src.test.java.ConstructorTest для данного класса включение Яндекс браузера происходит отдельно в самом классе

Для запуска тестов необходимо в консоли проекта ввести команду mvn clean test