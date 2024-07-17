#Backend #Registration #Smoke #Regression #Negative 

### Сообщение об ошибке при отправке запроса с пустым телом запроса

## Предусловия

1. {{baseUrl}} взять из файла https://gitlab.com/DJWOMS/junovnettestingdocs/-/blob/main/backend/baseUrl.md

## Шаги

1. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- тело запроса оставляем пустым (ничем не заполняем)

## Ожидаемый результат

Код ответа: 422 Unprocessable Entity

Пример body ответа:
```
{
    "detail": [
        {
            "type": "missing",
            "loc": [
                "body"
            ],
            "msg": "Field required",
            "input": null,
            "url": "https://errors.pydantic.dev/2.5/v/missing"
        }
    ]
}
```
### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | Cсылка на баг  |
|     ---     |  ---  |    ---      |   ---  |      ---       |
|  08.12.2023 | 20:10 |   passed    | @Baidak_Evgenii |       |
