---
navigation:
  - mysqli.stat.md: '« mysqli::stat'
  - mysqli.store-result.html: 'mysqli::storeresult »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::stmtinit'
---
# mysqli::stmtinit

# mysqlistmtinit

(PHP 5, PHP 7, PHP 8)

mysqli::stmtinit - mysqlistmtinit — Ініціалізує запит та повертає об'єкт для використання у mysqlistmtprepare

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::stmt_init(): mysqli_stmt|false
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_init(mysqli $mysql): mysqli_stmt|false
```

Виділяє пам'ять та ініціалізує об'єкт запиту, який можна використовувати у функції [mysqlistmtprepare()](mysqli-stmt.prepare.md)

> **Зауваження**
> 
> Усі наступні виклики mysqlistmt функцій викликають помилку, доки не буде викликана функція [mysqlistmtprepare()](mysqli-stmt.prepare.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

### Значення, що повертаються

Повертає об'єкт.

### Дивіться також

-   [mysqlistmtprepare()](mysqli-stmt.prepare.md) - готує затвердження SQL до виконання
