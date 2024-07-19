#Backend #Registration #Smoke #Regression #Positive

### Отправка запроса с заполнеными полями "password" и "password_confirm", паролем c набором из всех допустимых спецсимволов

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
  "email": "pigautiteve-7231@yopmail.com",
  "password": "1dA ![”]№:;'%<?>*(.)|_+-=,*/~`@#$^&{}",
  "telegram": "@Harishma12",
  "password_confirm": "1dA ![”]№:;'%<?>*(.)|_+-=,*/~`@#$^&{}",
  "is_mentor": true
}
```

## Ожидаемый результат

Код ответа: 201 Created

Пример body ответа:
```
{
    "id": 912,
    "first_name": "Екатерина-OBAMAЕ",
    "email": "pigautiteve-7231@yopmail.com",
    "telegram": "@Harishma12"
}
```

## Постусловие

Удалить из базы данных, созданного при выполнении тест-кейса пользователя 

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | Cсылка на баг  |
|     ---     |  ---  |    ---      |   ---  |      ---       |
|  08.12.2023 | 18:07 |    passed   | @Baidak_Evgenii |       |
