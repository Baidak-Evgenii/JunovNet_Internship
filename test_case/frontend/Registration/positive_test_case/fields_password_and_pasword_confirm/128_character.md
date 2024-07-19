#Frontend #Registration #Smoke #Regression #Positive

### Ввод в поля "Придумайте пароль" и "Повторите пароль", пароля из 128ми одинаковых, валидных символов

## Предусловия

1. {{baseUrl}} взять из файла https://gitlab.com/DJWOMS/junovnettestingdocs/-/blob/main/frontend/base_URL_register.md

## Шаги

1. Зайти на страницу {{baseUrl}} из предусловия

2. Ввести в поле "Придумайте пароль" - "jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBb!l2jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBbs" (вводить без кавычек "")

3. Ввести в поле "Повторите пароль" - "jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBb!l2jAm0A$+4kxs%Jq+FFp#KlWr042xDLkZr!oSiVGdvH#TT8HJGJm^L5ayNGL9hBbs" (вводить без кавычек "")

4. Кликнуть на странице за пределами полей для ввода

## Ожидаемый результат

Отсутствие сообщений об ошибке от полей "Придумайте пароль" и "Повторите пароль", поля приниманют введенные данные как валидные

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | ссылка на баг |
|     ---     |  ---  |    ---      |   ---  |      ---      |
|  08.12.2023 | 15:10 |   passed    | @Baidak_Evgenii |      |