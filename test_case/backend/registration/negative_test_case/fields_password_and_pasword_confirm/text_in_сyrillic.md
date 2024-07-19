#Backend #Registration #Smoke #Regression #Negative 

### Сообщение об ошибке при отправке запроса с заполненым текстом на кириллице полями "password" и "password_confirm"

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
  "password": "1AmЩЩЩЩЩ0A$+4ццццццs%Jq+",
  "telegram": "@Haris_hma12",
  "password_confirm": "1AmЩЩЩЩЩ0A$+4ццццццs%Jq+",
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
      "loc": [
        "string",
        0
      ],
      "msg": "string",
      "type": "string"
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
|  09.12.2023 | 18:07 |   failed   | @Baidak_Evgenii | https://gitlab.com/DJWOMS/junov_net/-/issues/37  |
