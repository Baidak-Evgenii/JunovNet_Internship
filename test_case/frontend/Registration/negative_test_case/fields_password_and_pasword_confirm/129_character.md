#Frontend #Registration #Smoke #Regression #Negative

### Сообщение об ошибке при вводе в поля "Придумайте пароль" и "Повторите пароль", пароля из 129ти одинаковых, валидных символов

## Предусловия

1. {{baseUrl}} взять из файла https://gitlab.com/DJWOMS/junovnettestingdocs/-/blob/main/frontend/base_URL_register.md

## Шаги

1. Зайти на страницу {{baseUrl}} из предусловия

2. Ввести в поле "Придумайте пароль" - "jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBb!l2jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBbFD" (вводить без кавычек "")

3. Ввести в поле "Повторите пароль" - "jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBb!l2jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBbFD" (вводить без кавычек "")

4. Кликнуть на странице за пределами полей для ввода

## Ожидаемый результат

Поле "Придумайте пароль" подсвечивается красным, под полем появляется текст подсказки, красного цвета - "Максимальная длина 128 символов"

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | ссылка на баг |
|     ---     |  ---  |    ---      |   ---  |      ---      |
|  08.12.2023 | 15:10 |   passed    | @Baidak_Evgenii |      |