#Backend #Registration #Smoke #Regression #Positive

### Отправка запроса с заполненым полем "email", емейлом с одним символом в емейле до знака @, всего в имени 7 символов

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
  "email": "j@jd.hg",
  "password": "123q56!A",
  "telegram": "@Haris_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```
## Ожидаемый результат

Код ответа: 201 Created

Пример body ответа:
```
{
    "id": 887,
    "first_name": "Екатерина-OBAMA",
    "email": "j@jd.hg",
    "telegram": "@Haris_hma12"
}
```

## Постусловие

Удалить из базы данных, созданного при выполнении тест-кейса пользователя 

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | Cсылка на баг  |
|     ---     |  ---  |    ---      |   ---  |      ---       |
|  08.12.2023 | 17:19 |   passed    | @Baidak_Evgenii |       |