---
navigation:
  - mysqlinfo.terminology.md: « Огляд термінології
  - mysqlinfo.library.choosing.md: Вибір бібліотеки »
  - index.md: PHP Manual
  - mysql.md: Огляд PHP драйверів MySQL
title: Вибір API
---
# Вибір API

PHP надає різні API для доступу до MySQL. Нижче показано API, що надаються модулями mysqli та PDO. У кожному прикладі коду створюється з'єднання з сервером MySQL, запущеним на сервері "example.com" з використанням логіну "user" і пароля "password" і виконується запит до нього.

**Приклад #1 Порівняння MySQL API**

```php
<?php
// mysqli
$mysqli = new mysqli("example.com", "user", "password", "database");
$result = $mysqli->query("SELECT 'Привет, дорогой пользователь MySQL!' AS _message FROM DUAL");
$row = $result->fetch_assoc();
echo htmlentities($row['_message']);

// PDO
$pdo = new PDO('mysql:host=example.com;dbname=database', 'user', 'password');
$statement = $pdo->query("SELECT 'Привет, дорогой пользователь MySQL!' AS _message FROM DUAL");
$row = $statement->fetch(PDO::FETCH_ASSOC);
echo htmlentities($row['_message']);
?>
```

*Порівняння можливостей*

Загальна продуктивність обох модулів приблизно однакова. Хоча продуктивність модуля становить лише частину загального часу виконання веб-запиту PHP, зазвичай трохи більше 0.1%.

|  | ext/mysqli | PDO\_MySQL |
| --- | --- | --- |
| З'явилося у версії PHP |  |  |
| Працює в PHP 7.x та 8.x | Так | Так |
| Статус розробки | Активний | Активний |
| Життєвий цикл | Активний | Активний |
| Рекомендовано для нових проектів | Так | Так |
| ООП інтерфейс | Так | Так |
| Процедурний інтерфейс | Так | Ні |
| API підтримує асинхронні, які не блокують запити mysqlnd | Так | Ні |
| Постійні (persistent) з'єднання | Так | Так |
| API підтримує кодування (charset) | Так | Так |
| API підтримує підготовлені запити на стороні сервера | Так | Так |
| API підтримує підготовлені запити на стороні клієнта | Ні | Так |
| API підтримує збережені процедури | Так | Так |
| API підтримує множинні запити | Так | Більшість |
| API підтримує транзакції | Так | Так |
| Можна контролювати транзакції за допомогою SQL | Так | Так |
| Підтримує всю функціональність MySQL 5.1+ | Так | Більшість |
