#Backend #Registration #Smoke #Regression #Negative

### Сообщение об ошибке при отправке запроса с заполнеными без строчных букв полями "password" и "password_confirm"


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
  "email": "lesonroitri-5850@yopmail.com",
  "password": "HTJK4 325@#$",
  "telegram": "@Haris_hma12",
  "password_confirm": "HTJK4 325@#$",
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
            "msg": "Value error, This password doesn't contains chars in uppercase and lowercase",
            "input": {
                "first_name": "Екатерина-OBAMA",
                "email": "lesonroitri-5850@yopmail.com",
                "password": "HTJK4 325@#$",
                "telegram": "@Haris_hma12",
                "password_confirm": "HTJK4 325@#$",
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
|     Дата    | Время | Результат   |   Имя  | Cсылка на баг  |
|     ---     |  ---  |    ---      |   ---  |      ---       |
|  09.12.2023 | 18:07 |  passed   | @Baidak_Evgenii |         |