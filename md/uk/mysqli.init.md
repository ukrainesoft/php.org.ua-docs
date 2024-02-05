---
navigation:
  - mysqli.info.md: '« mysqli::$info'
  - mysqli.insert-id.md: 'mysqli::$insert\_id »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::init'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::init

# mysqli\_init

(PHP 5, PHP 7, PHP 8)

mysqli::init -- mysqli\_init — Ініціалізує MySQLi та повертає об'єкт для використання у функції mysqli\_real\_connect()

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::init(): ?bool
```

Процедурний стиль

```methodsynopsis
mysqli_init(): mysqli|false
```

Виділяє пам'ять або ініціалізує об'єкт MySQL, придатний для використання у функціях [mysqli\_options()](mysqli.options.md)

> **Зауваження** :
> 
> Будь-які подальші виклики mysqli-функцій із цим ресурсом (крім [mysqli\_options()](mysqli.options.md)) зазнають невдачі, доки не буде викликана функція [mysqli\_real\_connect()](mysqli.real-connect.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод**mysqli::init()** повертає **`null`** у разі успішного виконання або **`false`**в случае возникновения ошибки. Функция**mysqli\_init()** повертає об'єкт у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Об'єктно-орієнтований стиль виклику методу **mysqli::init()** застарів. Замініть виклик методу **parent::init()** за допомогою **parent::\_\_construct()** |

### Приклади

Смотрите[mysqli\_real\_connect()](mysqli.real-connect.md)

### Дивіться також

-   [mysqli\_options()](mysqli.options.md) \- Встановлення налаштувань
-   [mysqli\_close()](mysqli.close.md) \- Закриває раніше відкрите з'єднання з базою даних
-   [mysqli\_real\_connect()](mysqli.real-connect.md) \- Встановлює з'єднання із сервером mysql
-   [mysqli\_connect()](function.mysqli-connect.md) \- Псевдонім mysqli::\_\_construct
