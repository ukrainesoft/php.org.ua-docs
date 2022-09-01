---
navigation:
  - mysqli.info.md: '« mysqli::$info'
  - mysqli.insert-id.html: 'mysqli::$insertid »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::init'
---
# mysqli::init

# mysqliinit

(PHP 5, PHP 7, PHP 8)

mysqli::init -- mysqliinit — Ініціалізує MySQLi та повертає об'єкт для використання у функції mysqlirealconnect()

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::init(): ?bool
```

Процедурний стиль

```methodsynopsis
mysqli_init(): mysqli|false
```

Виділяє пам'ять або ініціалізує об'єкт MySQL, придатний для використання у функціях [mysqlioptions()](mysqli.options.md)

> **Зауваження**
> 
> Будь-які подальші виклики mysqli-функцій із цим ресурсом (крім [mysqlioptions()](mysqli.options.md)) зазнають невдачі, доки не буде викликана функція [mysqlirealconnect()](mysqli.real-connect.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод **mysqli::init()** повертає **`null`** у разі успішного виконання або **`false`** у разі виникнення помилки. Функція **mysqliinit()** повертає об'єкт у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Об'єктно-орієнтований стиль виклику методу **mysqli::init()** застарів. Замініть виклик методу **parent::init()** за допомогою **parent::construct()** |

### Приклади

Дивіться [mysqlirealconnect()](mysqli.real-connect.html)

### Дивіться також

-   [mysqlioptions()](mysqli.options.md) - Встановлення налаштувань
-   [mysqliclose()](mysqli.close.md) - Закриває раніше відкрите з'єднання з базою даних
-   [mysqlirealconnect()](mysqli.real-connect.html) - Встановлює з'єднання із сервером mysql
-   [mysqliconnect()](function.mysqli-connect.html) - Псевдонім mysqli::construct
