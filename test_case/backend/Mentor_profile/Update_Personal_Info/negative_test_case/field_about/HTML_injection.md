#Mentor_profile #Main_information

#Сообщение об ошибке при отправке запроса с заполненым HTML иньекцией полем "about"

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
  "timezone": "(UTC-11:00) Midway Island",
  "position": "D_f4Зъ -ь_/ Я+я-S7Фщ)g&w8#N",
  "site": "D_f2З-_/5+-S()g&w9#N",
  "about": "<img src= "https://avatarko.ru/img/kartinka/2/zhivotnye_kot_prikol_ochki_1637.jpg">",
  "dev_experience": 10,
  "mentor_experience": 5
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
|  2023-10-18 | 17:46 |   passed    | Евгений|ссылка на баг|