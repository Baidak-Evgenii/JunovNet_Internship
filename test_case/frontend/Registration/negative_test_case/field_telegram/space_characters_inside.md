#Frontend #Registration #Smoke #Regression #Negative

### Сообщение об ошибке при вводе в c пробелом поле в строке "telegram", внутри самого telegram

Frontend #Registration #Smoke #Regression #Negative

### Сообщение об ошибке при вводе в поле "@telegram", имени с прообелом внутри самого имени

## Предусловия

1. {{baseUrl}} взять из файла https://gitlab.com/DJWOMS/junovnettestingdocs/-/blob/main/frontend/base_URL_register.md

## Шаги

1. Зайти на страницу {{baseUrl}} из предусловия

2. Ввести в поле "@telegram" - "@Hari_s ma123" (вводить без кавычек "")

3. Кликнуть на странице за пределами полей для ввода

## Ожидаемый результат

Поле "@telegram" подсвечивается красным, под поле появляется текст подсказки, красного цвета - "Логин может включать только буквы латиницы, цифры и нижнее подчеркивание"

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | Cсылка на баг  |
|     ---     |  ---  |    ---      |   ---  |      ---       |
|  08.12.2023 | 20:10 |   passed    | @Baidak_Evgenii |       |