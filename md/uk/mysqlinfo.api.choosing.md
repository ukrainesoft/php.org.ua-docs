- [« Огляд термінології](mysqlinfo.terminology.md)
- [Вибір бібліотеки »](mysqlinfo.library.choosing.md)

- [PHP Manual](index.md)
- [Огляд PHP драйверів MySQL](mysql.md)
- Вибір API

# Вибір API

PHP надає різні API для доступу до MySQL. Нижче показано API,
надані модулями mysqli та PDO. У кожному прикладі коду створюється
з'єднання з сервером MySQL запущеному на сервері "example.com"
використанням логіна "user" та пароля "password" та виконується запит до
ньому.

**Приклад #1 Порівняння MySQL API**

` <?php// mysqli$mysqli = new mysqli("example.com", "user", "password", "database"); ' AS _message FROM DUAL");$row = $result->fetch_assoc();echo htmlentities($row['_message']);// PDO$pdo = new PDO('mysql:host=example.com;db =database', 'user', 'password');$statement = $pdo->query("SELECT 'Привіт, дорогий користувач MySQL!' AS _message FROM DUAL");$row = $statement-> :FETCH_ASSOC);echo htmlentities($row['_message']);?> `

*Порівняння можливостей*

Загальна продуктивність обох модулів приблизно однакова. Хоча
продуктивність модуля становить лише частину загального часу
виконання веб-запиту PHP зазвичай не більше 0.1%.

|                                                          | ext/mysqli | PDO_MySQL |
| -------------------------------------------------------- | ---------- | --------- |
| З'явилося у версії PHP 5.0                               | 5.1        |           |
| Працює в PHP 7.x та 8.x                                  | Так        | Так       |
| Статус розробки Активний                                 | Активний   |           |
| Життєвий цикл Активний                                   | Активний   |           |
| Рекомендовано для нових проектів Так                     | Так        |           |
| ООП інтерфейс                                            | Так        | Так       |
| Процедурний інтерфейс Так                                | Ні         |           |
| API підтримує асинхронні, які не блокують запити mysqlnd | Так        | Ні        |
| Постійні з'єднання                                       | Так        | Так       |
| API підтримує кодування (charset) Так                    | Так        |           |
| API підтримує підготовлені запити на стороні сервера Так | Так        |           |
| API підтримує підготовлені запити на стороні клієнта Ні  | Так        |           |
| API підтримує процедури, що зберігаються                 | Так        | Так       |
| API підтримує множинні запити Так                        | Більшість  |           |
| API підтримує транзакції Так                             | Так        |           |
| Можна контролювати транзакції у вигляді SQL              | Так        | Так       |
| Підтримує всю функціональність MySQL 5.1+ Так            | Більшість  |           |
