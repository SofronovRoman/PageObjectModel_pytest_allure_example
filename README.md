<strong>Скрипт демонстрирует паттерн тестирования Page Object в связке с Selenium, Pytest и Allure. Осуществляется тестирование стартовой страницы 
Instagram (https://instagram.com). Представленный материал является учебным пособием.</strong>

Что такое Page Object?

Это популярный паттерн, который является де-факто стандартом в автоматизации тестирования веб-продуктов. Основная идея состоит в том, чтобы разделить логику тестов от 
реализации.Каждую веб-страницу проекта можно описать в виде объекта класса. Взаимодействие пользователя описываются в методах класса, а в тестах остается только 
бизнес-логика. Данный подход помогает избежать проблем с тестами при изменении верстки веб-приложения. Вам необходимо поправить только класс, описывающий страницу [[1]](https://habr.com/ru/post/472156/),
[[2]](https://selenium-python.readthedocs.io/page-objects.html), [[3]](https://www.youtube.com/watch?v=qBK5I_QApCg).

## Установка
```ruby
$ git clone https://github.com/SofronovRoman/PageObjectModel_pytest_allure_example.git
$ cd PageObjectModel_pytest_allure_example
$ pip install -r requirements.txt
```
## Настройка
Download [Chromedriver](https://chromedriver.chromium.org/downloads) for [Chrome](https://www.google.com/intl/en/chrome/)  
Добавьте в Config\config.py недостающие для тестирования данные (path_to_chromedriver, username и password Instagram)

## Использование
```ruby
$ pytest --alluredir=allure_report
$ allure serve allure_report
```

## Источники
Документация [Allure](https://docs.qameta.io/allure-report/)  
Документация [Pytest](https://docs.pytest.org/en/latest/contents.html#)  
Документация [Selenium](https://www.selenium.dev)
