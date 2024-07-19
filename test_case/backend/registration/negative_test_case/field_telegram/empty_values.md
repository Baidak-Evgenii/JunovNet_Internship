#Backend #Registration #Smoke #Regression #Negative 

### Сообщение об ошибке при отправке запроса без значения в паре ключ-знaчение в поле "telegram"

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
  "first_name": "Екатерина-OBAMAЕ",
  "email": "wecreussuveikeu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": ,
  "password_confirm": "123q56!A",
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
            "type": "json_invalid",
            "loc": [
                "body",
                131
            ],
            "msg": "JSON decode error",
            "input": {},
            "ctx": {
                "error": "Expecting value"
            }
        }
    ]
}
```

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | Cсылка на баг  |
|     ---     |  ---  |    ---      |   ---  |      ---       |
|  08.12.2023 | 20:10 |   passed    | @Baidak_Evgenii |       |