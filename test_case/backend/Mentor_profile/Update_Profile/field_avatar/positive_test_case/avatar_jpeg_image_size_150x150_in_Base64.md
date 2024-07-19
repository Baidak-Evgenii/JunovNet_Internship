#Mentor_profile #Main_information

#Успешное обновление данных профиля ментора, при заполнении поля avatar избражением формата jpeg с размером 150x150 пикселей в виде кода Base64

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
- ручка или эндпойнт: /mentor/profile/update
- Auth: Bearer Token
- Token: вставить сохранённый на шаге 3 access токен.
- Body запроса: 
{
  "avatar": "/9j/4AAQSkZJRgABAQEAYABgAAD//gA+Q1JFQVRPUjogZ2QtanBlZyB2MS4wICh1c2luZyBJSkcgSlBFRyB2ODApLCBkZWZhdWx0IHF1YWxpdHkK/9sAQwAIBgYHBgUIBwcHCQkICgwUDQwLCwwZEhMPFB0aHx4dGhwcICQuJyAiLCMcHCg3KSwwMTQ0NB8nOT04MjwuMzQy/9sAQwEJCQkMCwwYDQ0YMiEcITIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIy/8AAEQgAlgCWAwEiAAIRAQMRAf/EAB8AAAEFAQEBAQEBAAAAAAAAAAABAgMEBQYHCAkKC//EALUQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+v/EAB8BAAMBAQEBAQEBAQEAAAAAAAABAgMEBQYHCAkKC//EALURAAIBAgQEAwQHBQQEAAECdwABAgMRBAUhMQYSQVEHYXETIjKBCBRCkaGxwQkjM1LwFWJy0QoWJDThJfEXGBkaJicoKSo1Njc4OTpDREVGR0hJSlNUVVZXWFlaY2RlZmdoaWpzdHV2d3h5eoKDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uLj5OXm5+jp6vLz9PX29/j5+v/aAAwDAQACEQMRAD8A+f6KKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooA0tE0K+1++S1skTJZVaWVwkaFjtXcx4GScAdT2BqPTNMOpG5Y3Vvaw20XmyzT79oBZUAwisSSWHb1q54Tlk/wCEt0OLe3l/2lbtszxnzF5x61X0vVf7NgvIzY290lyiown34XDBh91h3UcHjjpQA3+ymm1OKxsLu3vnlHDw70Qdc5MirjAGScYA70+70Zreya8tr20vrdHCSvbF/wB0xzjcHVTg4PIBHbPSt+ytIBc2M8NmLa51LS7wLAjNtLbJUVk3En58FcZ5bOOCAMfSFZNC8QTMCIWtY4Qx6GQzxMF+u1HP0U0AYtFb/hqGOdbxdQRBo4VTdzEAPEedhjPeQ/MAvRhnOANys8TII7mBLaGJNLEf+hPFyJUzyzNgEvn72cYPGAABQBV03Qr7Vbe5uLdEWC3jkkeSVwinYhcqufvNtUnA579Oaj0zTDqRuWN1b2sNtF5ss0+/aAWVAMIrEklh29aueG5ZG1GSNnYomn321SeFzbS5wKr6Xqv9mwXkZsbe6S5RUYT78Lhgw+6w7qODxx0oAb/ZTTanFY2F3b3zyjh4d6IOucmRVxgDJOMAd6fd6M1vZNeW17aX1ujhJXti/wC6Y5xuDqpwcHkAjtnpW/ZWkAubGeGzFtc6lpd4FgRm2ltkqKybiT8+CuM8tnHBAGPpCsmheIJmBELWscIY9DIZ4mC/Xajn6KaAMWiiigAooooAKKKKACiiigAooooAfDNJbzRzQyPHLGwdHRiGVhyCCOhFTWWo32myNJY3lxbOwwxhkKbhnODjqKrUUATzXt1c3X2qe5mluMg+a8hZ8jpyeeKmvtY1LU1Rb/ULq6VCSomlZwCep5PX3qlRQAZOMZ49KMnGM8elFFAD4ppIXLxSPGxVkJRiCVYEEfQgkH1Bqay1G+02RpLG8uLZ2GGMMhTcM5wcdRVaigCea9urm6+1T3M0txkHzXkLPkdOTzxU19rGpamqLf6hdXSoSVE0rOAT1PJ6+9UqKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigD/9k=",
  "first_name": "Иван",
  "last_name": "Петров"
}

## Ожидаемый результат
1. Код ответа: 200 OK
2. Пример body ответа:
{
  "avatar": "string",
  "first_name": "string",
  "last_name": "string"
}

### Автор: Евгений

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | Баг № Trello|
|     ---     |  ---  |    ---      |   ---  |      ---    |
|  2023-11-04 | 13:49 |   passed    | Евгений|ссылка на баг|