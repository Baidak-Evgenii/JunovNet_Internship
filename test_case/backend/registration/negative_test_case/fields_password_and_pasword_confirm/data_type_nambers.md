#Backend #Registration #Smoke #Regression #Negative

### Сообщение об ошибке при отправке запроса с заполненым типом данных число полями "password" и "password_confirm"

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
  "email": "lesonipoitri-5850@yopmail.com",
  "password": 69,
  "telegram": "@Haris_hma12",
  "password_confirm": 69,
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
            "type": "string_type",
            "loc": [
                "body",
                "password"
            ],
            "msg": "Input should be a valid string",
            "input": 69,
            "url": "https://errors.pydantic.dev/2.5/v/string_type"
        },
        {
            "type": "string_type",
            "loc": [
                "body",
                "password_confirm"
            ],
            "msg": "Input should be a valid string",
            "input": 69,
            "url": "https://errors.pydantic.dev/2.5/v/string_type"
        }
    ]
}
```

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | Cсылка на баг  |
|     ---     |  ---  |    ---      |   ---  |      ---       |
|  08.12.2023 | 18:07 |  passed   | @Baidak_Evgenii |         |