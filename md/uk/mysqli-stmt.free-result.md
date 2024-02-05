---
navigation:
  - mysqli-stmt.field-count.md: '« mysqli\_stmt::$field\_count'
  - mysqli-stmt.get-result.md: 'mysqli\_stmt::get\_result »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::free\_result'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::free\_result

# mysqli\_stmt\_free\_result

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::free\_result -- mysqli\_stmt\_free\_result — Звільняє пам'ять від результату запиту, вказаного дескриптором

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::free_result(): void
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_free_result(mysqli_stmt $statement): void
```

Звільняє від результату запиту пам'ять, яка була зарезервована за допомогою [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.md)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.md) \- Зберігає набір результатів у внутрішньому буфері
