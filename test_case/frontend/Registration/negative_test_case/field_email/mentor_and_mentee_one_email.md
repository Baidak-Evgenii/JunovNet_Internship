#Frontend #Registration #Smoke #Regression #Negative

### Сообщение об ошибке в поле "Ваш e-mail", при попытке зарегистрировать на один емейл ментора и менти

## Предусловия

1. {{baseUrl}} взять из файла https://gitlab.com/DJWOMS/junovnettestingdocs/-/blob/main/frontend/base_URL_register.md

## Шаги

1. Зайти на страницу {{baseUrl}} из предусловия

2. Заполнить валидными данными все обязательные поля:
- поле "Как Вас зовут ?" - "Екатерина-OBAMA" (вводить без кавычек "")
- поле "Ваш e-mail" - "jefrauvEDakei-2155@yopmail.com" (вводить без кавычек "")
- поле "@telegram" - "@Haris_hma12m" (вводить без кавычек "")
- поле "Придумайте пароль" - "123q56!A" (вводить без кавычек "")
- поле "Повторите пароль" - "123q56!A" (вводить без кавычек "")

3. Кликнуть на чек-бокс "Стать ментором"

4. Кликнуть на кнопку "Зарегистрироваться"

5. На появившейся странице авторизации ввести код отправленный на емейл указанный в п 2.

6. Выйти из личного кабинета

7. Зайти на страницу {{baseUrl}} из предусловия

8. Заполнить валидными данными все обязательные поля:
- поле "Как Вас зовут ?" - "Екатерина-OBAMA" (вводить без кавычек "")
- поле "Ваш e-mail" - "jefrauvEDakei-2155@yopmail.com" (вводить без кавычек "")
- поле "@telegram" - "@Haris_hma12m" (вводить без кавычек "")
- поле "Придумайте пароль" - "123q56!A" (вводить без кавычек "")
- поле "Повторите пароль" - "123q56!A" (вводить без кавычек "")

9. Не кликать на чек-бокс "Стать ментором" - оставить чек-бокс не выбранным

10. Кликнуть на кнопку "Зарегистрироваться"

## Ожидаемый результат

Поле "Ваш e-mail" (после выполнения п. 10 из шагов воспроизведения) подсвечивается красным, под полем появляетится текст подсказки, красного цвета - "Данный email занят" 

## Постусловие

Удалить из базы данных, созданного при выполнении тест-кейса пользователя 

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | ссылка на баг |
|     ---     |  ---  |    ---      |   ---  |      ---      |
|  20.12.2023 | 11:23 |   passed    | @Baidak_Evgenii |      |