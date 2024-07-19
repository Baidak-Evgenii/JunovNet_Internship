#Backend #Registration #Smoke #Regression #Negative 

### Сообщение об ошибке при отправке запроса с заполненым c пробелом полем в строке "email", после всего еmail

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
  "email": "pigautitteve-7231@yopmail.com ",
  "password": "123q56!A",
  "telegram": "@Harishma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```
## Ожидаемый результат

Код ответа: 201 Created

Пример body ответа (возвращается без пробела который был в запросе):
```
{
  "first_name": "Екатерина-OBAMA",
  "email": "pigautitteve-7231@yopmail.com",
  "password": "123q56!A",
  "telegram": "@Haris_hma12",
  "password_confirm": "123q56!A",
  "is_mentor": true
}
```

## Постусловие

Удалить из базы данных, созданного при выполнении тест-кейса пользователя 

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | ссылка на баг |
|     ---     |  ---  |    ---      |   ---  |      ---      |
|  08.12.2023 | 18:57 |   passed    | @Baidak_Evgenii |      |
