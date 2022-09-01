---
navigation:
  - mysqli-stmt.field-count.html: '« mysqlistmt::$fieldcount'
  - mysqli-stmt.get-result.html: 'mysqlistmt::getresult »'
  - index.html: PHP Manual
  - class.mysqli-stmt.html: mysqlistmt
title: 'mysqlistmt::freeresult'
---
# mysqlistmt::freeresult

# mysqlistmtfreeresult

(PHP 5, PHP 7, PHP 8)

mysqlistmt::freeresult -- mysqlistmtfreeresult — Звільняє пам'ять від результату запиту, вказаного дескриптором

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::free_result(): void
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_free_result(mysqli_stmt $statement): void
```

Звільняє від результату запиту пам'ять, яка була зарезервована за допомогою [mysqlistmtstoreresult()](mysqli-stmt.store-result.html)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.html), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [mysqlistmtstoreresult()](mysqli-stmt.store-result.html) - Зберігає набір результатів у внутрішньому буфері
