# Реальный кейс компании «Ростелеком Информационные Технологии»

Дипломный проект: реальный кейс компании «Ростелеком Информационные Технологии»
Составлен план тестирования: https://docs.google.com/document/d/1EY_UKkr67uu7xYwO5ih11kgyBzr4Ddykezi-0rsS43A/edit
 
Ссылка на Google-таблицу с тест-кейсами: https://docs.google.com/spreadsheets/d/1otBRWGIxANHQZ9itCZ4LyLbi42BtP5qdguTecfqIWo8/edit#gid=0
В документе 1 лист: Тестирование требований заказчика. Найдены ошибки.
2 лист: Тест-кейсы. Проанализировано 30 кейсов с описанием шагов и ожидаемых результатов. Найдены баги.
3 лист. Баг-репорты. Составлен отчет с описанием названия, шагов воспроизведения, ожидаемый результат, фактический результат. Приложены скриншоты ошибок.
При создании тест-кейсов использованы техники:
- позитивного тестирования (ввод валидных данных для проверки работы системы в нормальных условиях);
- негативного тестирования (проверка невозможности доступа в личный кабинет при вводе некорректных данных (ввод несуществующих/пустых полей «email», «пароль» и т.п.), проверка наличия оповещения об ошибке доступа (с указанием, где ошибка));
- техника предугадывания ошибок (проверка наиболее вероятных типов дефектов, допускаемых при разработке);
- проверка граничных значений (проверка значений на границе допустимого диапазона входных данных (ввод  > 30 символов в полях «Имя», «Фамилия» и т.п.), которые могут привести к изменению поведения программы).
Проведено тестирование требований к системе (выявлены орфографические ошибки, логические ошибки).


В каталоге /pages располагаются файлы

base_page.py - описание класса BasePage - страница сайта
auth_page.py - описание класса AuthPage, наследующего BasePage - страница авторизации
locators.py - описание класса AuthLocators - используемые локаторы на странице авторизации
settings.py - данные об эл.почте, телефоне, пароле и другие, которые используются для тестов

В каталоге /tests располагаются файлы с тестами:

test_auth_page_elements.py - проверки наличия на странице авторизации всех описанных в требованиях элементов
test_positive_auth.py - реализация позитивных тест-кейсов авторизации пользователя в ЛК Ростелеком
test_negative_auth.py - реализация негативных тест-кейсов авторизации пользователя в ЛК Ростелеком

В корне

conftest.py - фикстура с веб-драйвером и пост-обработкой ошибки
requirements.txt - файл с требуемыми для проекта библиотеками (pytest, pytest-selenium, selenuim)
