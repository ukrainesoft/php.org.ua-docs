---
navigation:
  - mysqli.begin-transaction.md: '« mysqli::begintransaction'
  - mysqli.character-set-name.md: 'mysqli::charactersetname »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::changeuser'
---
# mysqli::changeuser

# mysqlichangeuser

(PHP 5, PHP 7, PHP 8)

mysqli::changeuser -- mysqlichangeuser — Дозволяє змінити користувача підключеного до бази даних

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::change_user(string $username, string $password, ?string $database): bool
```

Процедурний стиль

```methodsynopsis
mysqli_change_user(    mysqli $mysql,    string $username,    string $password,    ?string $database): bool
```

Змінює користувача, від імені якого здійснено підключення до бази даних, та встановлює поточну базу даних

Для успішної зміни користувача необхідні коректні `username` і `password`а також наявність достатніх прав для роботи з базою. Якщо зміна користувача закінчиться помилкою, збережеться поточна авторизація користувача до виклику функції.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

`username`

Ім'я користувача для доступу до MySQL

`password`

Пароль для доступу до MySQL

`database`

Ім'я бази даних

Якщо потрібно змінити користувача без вибору бази даних, слід вказувати **`null`**. Для вибору бази даних необхідно використовувати функцію [mysqliselectdb()](mysqli.select-db.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqli::changeuser()****

Об'єктно-орієнтований стиль

```php
<?php

/* создаём подключение к базе данных test */
$mysqli = new mysqli("localhost", "my_user", "my_password", "test");

/* проверяем соединение */
if (mysqli_connect_errno()) {
    printf("Подключение не удалось: %s\n", mysqli_connect_error());
    exit();
}

/* устанавливаем переменную a */
$mysqli->query("SET @a:=1");

/* все сбрасываем и выбираем новую базу данных */
$mysqli->change_user("my_user", "my_password", "world");

if ($result = $mysqli->query("SELECT DATABASE()")) {
    $row = $result->fetch_row();
    printf("База данных по умолчанию: %s\n", $row[0]);
    $result->close();
}

if ($result = $mysqli->query("SELECT @a")) {
    $row = $result->fetch_row();
    if ($row[0] === NULL) {
        printf("Значение переменной - NULL\n");
    }
    $result->close();
}

/* закрываем соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
/* создаём подключение к базе данных test */
$link = mysqli_connect("localhost", "my_user", "my_password", "test");

/* проверяем соединение */
if (!$link) {
    printf("Подключение не удалось: %s\n", mysqli_connect_error());
    exit();
}

/* устанавливаем переменную a */
mysqli_query($link, "SET @a:=1");

/* все сбрасываем и выбираем новую базу данных */
mysqli_change_user($link, "my_user", "my_password", "world");

if ($result = mysqli_query($link, "SELECT DATABASE()")) {
    $row = mysqli_fetch_row($result);
    printf("База данных по умолчанию: %s\n", $row[0]);
    mysqli_free_result($result);
}

if ($result = mysqli_query($link, "SELECT @a")) {
    $row = mysqli_fetch_row($result);
    if ($row[0] === NULL) {
        printf("Значение переменной - NULL\n");
    }
    mysqli_free_result($result);
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
База данных по умолчанию: world
Значение переменной - NULL
```

### Примітки

> **Зауваження**
> 
> В результаті виклику функції поточне з'єднання з базою даних починає поводитися так, ніби було створено нове з'єднання. Незалежно від результату операції, виклик функції призводить до відкату всіх активних транзакцій, закриття тимчасових таблиць та розблокування всіх заблокованих таблиць.

### Дивіться також

-   [mysqliconnect()](function.mysqli-connect.md) - Псевдонім mysqli::construct
-   [mysqliselectdb()](mysqli.select-db.md) - Встановлює базу даних для запитів, що виконуються.
