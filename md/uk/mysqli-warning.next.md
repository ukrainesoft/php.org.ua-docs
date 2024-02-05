---
navigation:
  - mysqli-warning.construct.md: '« mysqli\_warning::\_\_construct'
  - class.mysqli-sql-exception.md: mysqli\_sql\_exception »
  - index.md: PHP Manual
  - class.mysqli-warning.md: mysqli\_warning
title: 'mysqli\_warning::next'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_warning::next

(PHP 5, PHP 7, PHP 8)

mysqli\_warning::next — Отримує таке попередження

### Опис

```methodsynopsis
public mysqli_warning::next(): bool
```

Змінює інформацію про попередження на наступне попередження, якщо це можливо.

Після того, як попередження було встановлено на наступне попередження, доступні нові значення властивостей `message` `sqlstate`и`errno`из[mysqli\_warning](class.mysqli-warning.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо наступне попередження було отримано успішно. Якщо більше немає попереджень, поверне **`false`**
