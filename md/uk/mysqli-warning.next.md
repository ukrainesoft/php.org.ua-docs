---
navigation:
  - mysqli-warning.construct.html: '« mysqliwarning::construct'
  - class.mysqli-sql-exception.html: mysqlisqlexception »
  - index.md: PHP Manual
  - class.mysqli-warning.html: mysqliwarning
title: 'mysqliwarning::next'
---
# mysqliwarning::next

(PHP 5, PHP 7, PHP 8)

mysqliwarning::next — Отримує таке попередження

### Опис

```methodsynopsis
public mysqli_warning::next(): bool
```

Змінює інформацію про попередження на наступне попередження, якщо це можливо.

Після того, як попередження було встановлено на наступне попередження, доступні нові значення властивостей `message` `sqlstate` і `errno` з [mysqliwarning](class.mysqli-warning.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо наступне попередження було отримано успішно. Якщо більше немає попереджень, поверне **`false`**
