---
navigation:
  - mysqli.stat.md: '« mysqli::stat'
  - mysqli.store-result.md: 'mysqli::store\_result »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::stmt\_init'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::stmt\_init

# mysqli\_stmt\_init

(PHP 5, PHP 7, PHP 8)

mysqli::stmt\_init -- mysqli\_stmt\_init — Ініціалізує запит та повертає об'єкт для використання у mysqli\_stmt\_prepare

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::stmt_init(): mysqli_stmt|false
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_init(mysqli $mysql): mysqli_stmt|false
```

Виділяє пам'ять та ініціалізує об'єкт запиту, який можна використовувати у функції [mysqli\_stmt\_prepare()](mysqli-stmt.prepare.md)

> **Зауваження** :
> 
> Усі наступні виклики mysqli\_stmt функцій викликають помилку, доки не буде викликана функція [mysqli\_stmt\_prepare()](mysqli-stmt.prepare.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Повертає об'єкт.

### Дивіться також

-   [mysqli\_stmt\_prepare()](mysqli-stmt.prepare.md) \- готує затвердження SQL до виконання
