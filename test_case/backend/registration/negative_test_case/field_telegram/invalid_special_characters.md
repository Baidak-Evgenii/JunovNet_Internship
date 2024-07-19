#Backend #Registration #Smoke #Regression #Negative

### Сообщение об ошибке при отправке запроса с заполненым полем "telegram", с недопустимыми спецсимволами

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
  "first_name": "релгнжщэз",
  "email": "wecreussuveikeu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Hari!s_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

2. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгжщэз",
  "email": "Wecreussuveikeu-2230@yopmail.coнm",
  "password": "123q56!A",
  "telegram": "@Hari"s_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

3. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "WEcreussuveikeu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har№is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

4. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "WECreussuveikeu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Ha;ris_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

5. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "WECReussuveikeu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har%is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

6. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "WECREussuveikeu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har?is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

7. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "WECREUssuveikeu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Hari*s_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

8. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "WECREUSsuveikeu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har(is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

9. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "WECREUSSuveikeu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Ha)ris_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

10. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "WECREUSSUveikeu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har\is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

11. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "WECREUSSUVeikeu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Ha+ris_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

12. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "WECREUSSUVEikeu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har=is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

13. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "WECREUSSUVEIkeu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har,is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

14. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "WECREUSSUVEIKEu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har/is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

15. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "WECREUSSUVEIKEU-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har~is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

16. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "WECREUSSUVEIKEU_2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Ha`ris_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

17. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "wECREUSSUVEIKEU-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har@is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

18. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "weCREUSSUVEIKEU-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Hari#s_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

19. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "wecREUSSUVEIKEU-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Hari$s_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

20. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "wecrEUSSUVEIKEU-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har^is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

21. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "wecreUSSUVEIKEU-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har&is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

22. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "wecreuSSUVEIKEU-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har{is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

23. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "wecreusSUVEIKEU-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har}is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

24. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "wecreussUVEIKEU-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har[is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

25. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "wecreussuVEIKEU-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Ha]ris_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

26. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "wecreussuvEIKEU-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Ha:ris_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

27. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "wecreussuvеiKEU-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har<is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

28. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "wecreussuvеikEU-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har>is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

29. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "wecreussuvеikeU-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har.is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

30. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "ecreussuvеikeu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har|is_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

31. Отправить запрос в Postman
- тип запроса: POST
- ручка она же эндпойнт: {{baseUrl}}/auth/registration
- Auth: No Auth
- Body запроса (Комментарий: так как проверка был ли ранее создан подобный пользователь происходит по email, то при каждом запросе необходимо придумать новый - ранее не применявшийся email (для этого можно использовать генератор email https://yopmail.com/ru/email-generator)): 
```
{
  "first_name": "релгнжщэз",
  "email": "ecreussuvеikeu-2230@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Har-is_hma12",
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
                "body"
            ],
            "msg": "Value error, telegram must contain only Latin characters or a symbol '_'",
            "input": {
                "first_name": "релгнжщэз",
                "email": "wecreussuveikeu-2230@yopmail.com",
                "password": "123q56!A",
                "telegram": "@Hari!s_hma12", // comment в значении ключа "telegram" будет то, что вы отправляете в запросе
                "password_confirm": "123q56!A",
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
|     Дата    | Время | Результат   |   Имя  | ссылка на баг |
|     ---     |  ---  |    ---      |   ---  |      ---      |
|  08.12.2023 | 18:50 |   failed   | @Baidak_Evgenii | https://gitlab.com/DJWOMS/junov_net/-/issues/34 |