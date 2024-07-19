#Frontend #Registration #Smoke #Regression #Negative

### Сообщение об ошибке при вводе в поле "Ваш e-mail", емейла с тире в конце поддомена

## Предусловия

1. {{baseUrl}} взять из файла https://gitlab.com/DJWOMS/junovnettestingdocs/-/blob/main/frontend/base_URL_register.md

## Шаги

1. Зайти на страницу {{baseUrl}} из предусловия

2. Ввести в поле "Ваш e-mail" - "test@9m-.com" (вводить без кавычек "")

3. Кликнуть на странице за пределами полей для ввода

## Ожидаемый результат

Поле "Ваш e-mail" подсвечивается красным, под поле появляется текст подсказки, красного цвета - "Неверный формат"

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | ссылка на баг |
|     ---     |  ---  |    ---      |   ---  |      ---      |
|  11.12.2023 | 00:05 |   failed    | @Baidak_Evgenii | https://gitlab.com/DJWOMS/front/-/issues/15 |
