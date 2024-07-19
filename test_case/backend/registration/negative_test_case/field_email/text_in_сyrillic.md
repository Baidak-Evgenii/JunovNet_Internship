#Backend #Registration #Smoke #Regression #Negative 

### Сообщение об ошибке при отправке запроса с заполненым полем "еmail", емейлом с текстом на кириллице

## Предусловия

1. {{baseUrl}} взять из файла https://gitlab.com/DJWOMS/junovnettestingdocs/-/blob/main/backend/baseUrl.md

## Шаги

1. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "Екатерина-OBAMA",
  "email": "москва@москва.рф",
  "password": "123456!A",
  "telegram": "@Haris_hma12",
  "password_confirm": "123456!A",
  "is_mentor": true
}
```
## Ожидаемый результат

Код ответа: 422 Validation Error

Пример body ответа:
```
{
    "detail": [
        {
            "type": "value_error",
            "loc": [
                "body"
            ],
            "msg": "Value error, invalid email",
            "input": {
                "first_name": "Екатерина-OBAMA",
                "email": "москва@москва.рф",
                "password": "123456!A",
                "telegram": "@Haris_hma12",
                "password_confirm": "123456!A",
                "is_mentor": true
            },
            "ctx": {
                "error": {}
            },
            "url": "https://errors.pydantic.dev/2.5/v/value_error"
        }
    ]
}
```

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | ссылка на баг |
|     ---     |  ---  |    ---      |   ---  |      ---      |
|  08.12.2023 | 18:57 |   passed    | @Baidak_Evgenii |      |
