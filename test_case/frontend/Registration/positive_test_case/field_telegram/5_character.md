#Frontend #Registration #Smoke #Regression #Positive

### Ввод в поле "@telegram", имени из 5х символов

## Предусловия

1. {{baseUrl}} взять из файла https://gitlab.com/DJWOMS/junovnettestingdocs/-/blob/main/frontend/base_URL_register.md

## Шаги

1. Зайти на страницу {{baseUrl}} из предусловия

2. Ввести в поле "@telegram" - "@Hari" (вводить без кавычек "")

3. Кликнуть на странице за пределами полей для ввода

## Ожидаемый результат

Отсутствие сообщений об ошибке от поля "@telegram", поле приниманет введенные данные как валидные

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | ссылка на баг |
|     ---     |  ---  |    ---      |   ---  |      ---      |
|  08.12.2023 | 15:10 |   passed    | @Baidak_Evgenii |      |