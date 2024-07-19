#Mentor_profile #Main_information

#Ошибка при обновлении данных профиля ментора, если поле "avatar" не заполнено

#smoke,regression

## Предварительные условия
1. Данные для авторизации и аутентификации под аккаунтом ментора находится в файле по ссылке:
 https://gitlab.com/DJWOMS/junovnettestingdocs/-/blob/main/backend/Authorization_data_mentor.md?ref_type=heads
2. URL для авторизации и отправки запросов в Postman к бэкенду находится в файле по ссылке:
 https://gitlab.com/DJWOMS/junovnettestingdocs/-/blob/main/backend/baseUrl.md?ref_type=heads

## Шаги
1. Пройти авторизацию в Swagger JunovNet
- URL находится в файле по ссылке в предусловиях п.2, к URL добавить путь /docs
- данные для авторизации (необходимо ввести username и password) находится в файле по ссылке в предусловиях п.1 

2. Пройти аутентификацию в Postman или в Swagger JunovNet
- отправить POST запрос с эндпойнтом (ручкой) /auth/login по URL находящемуся в файле по ссылке в предусловиях п.2
- Body запроса (необходимо ввести email и password из файла по ссылке в предусловиях п.1): 
{
  "email": "string",
  "password": "string"
}

3. Сохранить полученный в ответе access токен.

4. Отправить запрос в Postman
- тип запроса: PATCH
- ручка или эндпойнт: /mentor/profile/info
- Auth: Bearer Token
- Token: вставить сохранённый на шаге 3 access токен.
- Body запроса:
{
  "avatar": "",
  "first_name": "Иван",
  "last_name": "Петров"
}

## Ожидаемый результат
1. Код ответа: 422 Validation Error
2. Пример body ответа:
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

### Автор: Евгений

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | Баг № Trello|
|     ---     |  ---  |    ---      |   ---  |      ---    |
|  2023-10-18 | 17:41 |   failed    | Евгений|https://trello.com/c/jZ7czN6H/29-%D0%BA%D0%BE%D0%B4-%D0%BE%D1%82%D0%B2%D0%B5%D1%82%D0%B0-200-%D0%B2%D0%BC%D0%B5%D1%81%D1%82%D0%BE-422-%D0%BF%D1%80%D0%B8-%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81%D0%B5-%D1%81-%D0%BF%D1%83%D1%81%D1%82%D1%8B%D0%BC-%D0%BD%D0%B5%D0%B7%D0%B0%D0%BF%D0%BE%D0%BB%D0%BD%D0%B5%D0%BD%D0%BD%D1%8B%D0%BC-%D0%B7%D0%BD%D0%B0%D1%87%D0%B5%D0%BD%D0%B8%D0%B5%D0%BC-%D0%BA%D0%BB%D1%8E%D1%87%D0%B0-about-%D0%BC%D0%B5%D1%82%D0%BE%D0%B4-patch-%D1%80%D1%83%D1%87%D0%BA%D0%B0-mentor-profile-info|