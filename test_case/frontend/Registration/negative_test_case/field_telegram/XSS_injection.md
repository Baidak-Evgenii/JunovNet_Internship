#Frontend #Registration #Smoke #Regression #Negative

### Сообщение об ошибке при вводе в поле "@telegram" XSS инъекции

## Предусловия

1. {{baseUrl}} взять из файла https://gitlab.com/DJWOMS/junovnettestingdocs/-/blob/main/frontend/base_URL_register.md

## Шаги

1. Зайти на страницу {{baseUrl}} из предусловия

2. Ввести в поле "@telegram" - "@<script>alert()</script>" (вводить без кавычек "")

3. Поставить курсор (кликнуть указателем мыши) в тексте поля "@telegram", между @ и <script>alert()</script>. Затем нажать Backspace, после чего в поле должен остаться только текст <script>alert()</script>

4. Кликнуть на странице за пределами полей для ввода

## Ожидаемый результат

Поле "@telegram" подсвечивается красным, под поле появляется текст подсказки, красного цвета - "Логин должен начинаться с @"

### Автор: @Baidak_Evgenii

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | Cсылка на баг  |
|     ---     |  ---  |    ---      |   ---  |      ---       |
|  08.12.2023 | 20:10 |   passed    | @Baidak_Evgenii |       |