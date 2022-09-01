---
navigation:
  - mysqli-result.field-seek.html: '« mysqliresult::fieldseek'
  - mysqli-result.getiterator.html: 'mysqliresult::getIterator »'
  - index.md: PHP Manual
  - class.mysqli-result.html: mysqliresult
title: 'mysqliresult::free'
---
# mysqliresult::free

# mysqliresult::close

# mysqliresult::freeresult

# mysqlifreeresult

(PHP 5, PHP 7, PHP 8)

mysqliresult::free -- mysqliresult::close -- mysqliresult::freeresult -- mysqlifreeresult — Звільняє пам'ять, зайняту результатами запиту

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::free(): void
```

```methodsynopsis
public mysqli_result::close(): void
```

```methodsynopsis
public mysqli_result::free_result(): void
```

Процедурний стиль

```methodsynopsis
mysqli_free_result(mysqli_result $result): void
```

Визволяє пам'ять, зайняту результатами запиту.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqliresult](class.mysqli-result.html), отриманий за допомогою [mysqliquery()](mysqli.query.md) [mysqlistoreresult()](mysqli.store-result.html) [mysqliuseresult()](mysqli.use-result.html) або [mysqlistmtgetresult()](mysqli-stmt.get-result.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [mysqliquery()](mysqli.query.md) - Виконує запит до бази даних
-   [mysqlistmtgetresult()](mysqli-stmt.get-result.md) - Отримує результат із підготовленого запиту у вигляді об'єкта mysqliresult
-   [mysqlistoreresult()](mysqli.store-result.md) - передає на клієнта результуючий набір останнього запиту
-   [mysqliuseresult()](mysqli.use-result.md) - Готує результуючий набір на сервері для використання
