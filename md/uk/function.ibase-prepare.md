---
navigation:
  - function.ibase-pconnect.md: « ibase\_pconnect
  - function.ibase-query.md: ibase\_query »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_prepare
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_prepare

(PHP 5, PHP 7 < 7.4.0)

ibase\_prepare — Підготовка запиту для подальшого зв'язування псевдозмінних та виконання

### Опис

```methodsynopsis
ibase_prepare(string $query): resource
```

```methodsynopsis
ibase_prepare(resource $link_identifier, string $query): resource
```

```methodsynopsis
ibase_prepare(resource $link_identifier, string $trans, string $query): resource
```

Підготовляє запит для подальшого зв'язування псевдозмінних та виконання (за допомогою [ibase\_execute()](function.ibase-execute.md)

### Список параметрів

`query`

Запит InterBase.

`link_identifier`

Ідентифікатор посилання InterBase, який повертається функцією [ibase\_connect()](function.ibase-connect.md). Якщо не вказано, передбачається останнє відкрите посилання.

`trans`

Дескриптор транзакції InterBase, з якою має бути пов'язаний запит. Якщо не вказано, передбачається транзакція стандартного з'єднання.

### Значення, що повертаються

Повертає дескриптор підготовленого запиту або \*\*`false`\*\*в случае возникновения ошибки.
