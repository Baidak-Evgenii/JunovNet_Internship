#Mentor_profile #Main_information

#Сообщение об ошибке при отправке запроса с незаполненым полем "position"

#smoke,regression

## Предварительные условия
1. Данные для авторизации и аутентификации под аккаунтом ментора (Необходимы username и password):

- username: mentor
- password: mentor

## Шаги
1. Пройти авторизацию в Swagger JunovNet
- URL: http://82.147.71.207:8000/docs
- данные для авторизации - см. предусловие

2. Пройти аутентификацию в Postman или в Swagger JunovNet
- отправить POST-запрос /auth/login
- Body запроса: 
{
  "email": "mentor@mentor.com",
  "password": "mentor"
}

3. Сохранить полученный в ответе access токен.

4. Отправить запрос в Postman
- тип запроса: PATCH
- URL: http://82.147.71.207:8000/mentor/profile/info
- Auth: Bearer Token
- Token: вставить сохранённый на шаге 3 access токен.
- Body запроса: 
{
  "timezone": "(UTC-11:00) Midway Island",
  "position": "",
  "site": "D_f Зъ -ь_/ Я+я-S(Фщ)g&w #N",
  "about": "Hello, мир! This is a тестовый текст с разными символами -_/+()#!2@&^% просто для проверки, как работает генерация. 1234567890Hello, мир! This is a тестовый текст с разными символами -_/+()#!2@&^% просто для п-_/+()#!2@&^%  роверки, как работает генерация.",
  "dev_experience": 10,
  "mentor_experience": 5
}

## Ожидаемый результат
1. Код ответа: 422 Validation Error
2. Пример body ответа:
{
  "detail": [
    {
      "loc": [
        "string",
        0
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}

### Автор: Евгений

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | Баг № Trello|
|     ---     |  ---  |    ---      |   ---  |      ---    |
|  2023-10-13 | 20:20 |   passed    | Евгений|ссылка на баг|