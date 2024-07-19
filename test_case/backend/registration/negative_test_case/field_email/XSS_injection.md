#Backend #Registration #Smoke #Regression #Negative #Smoke #Regression

### Сообщение об ошибке при отправке запроса с заполненым XSS инъекцией полем "еmail"

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
  "email": "<script>alert()</script>",
  "password": "123q56!A",
  "telegram": "@Harishma12",
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
            "type": "value_error",
            "loc": [
                "body",
                "email"
            ],
            "msg": "value is not a valid email address: An email address cannot have two periods in a row.",
            "input": "jfnhf.gkmjl@lf.h..f",
            "ctx": {
                "reason": "An email address cannot have two periods in a row."
            }
        }
    ]
}
```

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | ссылка на баг |
|     ---     |  ---  |    ---      |   ---  |      ---      |
|  08.12.2023 | 18:58 |   passed    | @Baidak_Evgenii |      |
