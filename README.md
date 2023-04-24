Тестирование регистрации и авторизации в Личном Кабинете Ростелеком. https://b2c.passport.rt.ru 

При тестировании применялись техники тест-дизайна: пограничные значения, эквивалентное разделение, предугадывание ошибок, исследовательское тестирование, парамертизация тестов. 

Проект выполнен на Python 3.10 

Использовались библиотеки Pytest и Selenium Браузер Yandex Browser 110.0.5481.806 (64-разрядная версия) и yandexdriver для этой версии, который можно скачать и использовать по ссылке https://github.com/yandex/YandexDriver. 

Проект содержит следующие файлы и папки: 

1.conftest.py — содержит весь необходимый код для отлова неудачных тестовых случаев и создания скриншота страницы в случае, если какой-либо тестовый пример не сработает. 

2.pages/base.py — содержит реализацию шаблона PageObject для Python. 

3.pages/auth_locators.py — это локаторы страницы авторизации для работы с автотестами. 

4.pages/elements.py — содержит вспомогательный класс для определения веб-элементов на веб-страницах. 

5.test_rostelecom.py — содержит тесты для ЛК Ростелеком.       

6.utilities.py — содержит необходимые входные тестовые данные.

Запуск тестов: 

1.Установите все требования: pip install -r requirements.txt 

2.Загрузите Selenium WebDriver с https://chromedriver.chromium.org/downloads, если у вас Google Chrome и https://github.com/yandex/YandexDriver если у вас Yandex Browser (выберите версию, совместимую с вашим браузером) 

3.Запустите тесты все тесты разом командой из терминала: python -m pytest -v --driver Chrome --driver-path C:/yandexdriver.exe, где C:/yandexdriver.exe путь до yandexdriver.exe
 
 3.1 Либо запустить каждый тест по отдельности: pytest RSTLK_Tests.py::test_name --driver Chrome --driver-path C:/yandexdriver.exe где test_name название теста, который хотим запустить.
