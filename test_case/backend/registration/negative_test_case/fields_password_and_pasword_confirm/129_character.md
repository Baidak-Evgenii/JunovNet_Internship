#Backend #Registration #Smoke #Regression #Negative

### Сообщение об ошибке при отправке запроса с заполнеными одинаковыми 129 символоми полями "password" и "password_confirm"

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
  "password": "jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBb!l2jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBbFD",
  "telegram": "@Haris_hma12",
  "password_confirm": "jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBb!l2jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBbFD",
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
            "msg": "Value error, This password is too long. It must contain not more than 64 characters.",
            "input": {
                "first_name": "Екатерина-OBAMAЕ",
                "email": "wecreussuveikeu-2230@yopmail.com",
                "password": "jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBb!l2jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBbFD",
                "telegram": "@Haris_hma12",
                "password_confirm": "jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBb!l2jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBbFD",
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

## Постусловие

Удалить из базы данных, созданного при выполнении тест-кейса пользователя

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | Cсылка на баг  |
|     ---     |  ---  |    ---      |   ---  |      ---       |
|  08.12.2023 | 18:07 |   failed   | @Baidak_Evgenii | https://gitlab.com/DJWOMS/junov_net/-/issues/29  |