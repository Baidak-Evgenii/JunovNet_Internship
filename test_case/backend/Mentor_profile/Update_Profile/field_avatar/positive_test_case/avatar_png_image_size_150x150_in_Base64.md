#Mentor_profile #Main_information

#Успешное обновление данных профиля ментора, при заполнении поля avatar избражением формата png с размером 150x150 пикселей в виде кода Base64

#smoke,regression

## Предварительные условия
1. Данные для авторизации и аутентификации под аккаунтом ментора находится в файле по ссылке:
 https://gitlab.com/DJWOMS/junovnettestingdocs/-/blob/main/backend/Authorization_data_mentor.md?ref_type=heads
2. URL для авторизации и отправки запросов в Postman к бэкенду находится в файле по ссылке:
 https://gitlab.com/DJWOMS/junovnettestingdocs/-/blob/main/backend/baseUrl.md?ref_type=heads

## Шаги
1. Пройти авторизацию в Swagger JunovNet
- URL находится в файле по ссылке в предусловиях п.2, к URL добавить путь /docs
- данные для авторизации (необходимо ввести username и password) находится в файле по ссылке в предусловиях п.1 

2. Пройти аутентификацию в Postman или в Swagger JunovNet
- отправить POST запрос с эндпойнтом (ручкой) /auth/login по URL находящемуся в файле по ссылке в предусловиях п.2
- Body запроса (необходимо ввести email и password из файла по ссылке в предусловиях п.1): 
{
  "email": "string",
  "password": "string"
}

3. Сохранить полученный в ответе access токен.

4. Отправить запрос в Postman
- тип запроса: PATCH
- ручка или эндпойнт: /mentor/profile/update
- Auth: Bearer Token
- Token: вставить сохранённый на шаге 3 access токен.
- Body запроса: 
{
  "avatar": "iVBORw0KGgoAAAANSUhEUgAAAJYAAACWBAMAAADOL2zRAAAAG1BMVEUAAAD///8fHx+fn59fX1+/v7/f399/f38/Pz92BP0oAAAACXBIWXMAAA7EAAAOxAGVKw4bAAAA+0lEQVRoge3RzUrDQBiF4cMkxVzGoERcBtrSLrPwZxsq1Sx7CYJ1H1Dxtp2JyTiBEMaNq/fZzMeB7zCTSAAAAAAAAADwP66k7HisZLbPcWyq+XxJ/iSt/FDavInyu9N8vuR11V9N2kvn3/iiambzJUU9drnd0h21dOOODzXTPInr+ips/338mzYyrYaOOE/tut+9dcWwk9VlN3bFeWrXpXQIO7ufa/muSZ7Y5ZzDW65fQtckT++69bt+NO0m7gr5H7r2OkgPbii7rI66Qp7aZVWc9C7j1tT6Xzl0xXlq1+d6bZU/bjv5fZmxK86T9dvGJucAAAAAAAAAEPsG6kYkDhZMtN0AAAAASUVORK5CYII=",
  "first_name": "Иван",
  "last_name": "Петров"
}

## Ожидаемый результат
1. Код ответа: 200 OK
2. Пример body ответа:
{
  "avatar": "string",
  "first_name": "string",
  "last_name": "string"
}

### Автор: Евгений

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | Баг № Trello|
|     ---     |  ---  |    ---      |   ---  |      ---    |
|  2023-11-04 | 13:49 |   passed    | Евгений|ссылка на баг|