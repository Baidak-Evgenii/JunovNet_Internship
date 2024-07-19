#Mentor_profile #Main_information

#Успешное обновление данных профиля ментора, при заполнении поля avatar избражением формата png с размером 549x1321 пикселей в виде кода Base64

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
  "avatar": "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",
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