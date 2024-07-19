#Frontend #Registration #Smoke #Regression #Positive

### Переход на страницу авторизации после клика по тексту "Войдите"

## Предусловия

1. {{baseUrl}} взять из файла https://gitlab.com/DJWOMS/junovnettestingdocs/-/blob/main/frontend/base_URL_register.md

## Шаги

1. Зайти на страницу {{baseUrl}} из предусловия

2. Найти текст "Это займет не более 2 минут. Уже зарегистрированы? Войдите"

3. Кликнуть по слову "Войдите" из текста в п. 2

## Ожидаемый результат

Происходит переход на страницу авторизации (https://junov-net.netlify.app/login)

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | ссылка на баг |
|     ---     |  ---  |    ---      |   ---  |      ---      |
|  17.12.2023 | 00:54 |   failed    | @Baidak_Evgenii | https://gitlab.com/DJWOMS/front/-/issues/48 |
