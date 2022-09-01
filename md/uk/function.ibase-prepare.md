---
navigation:
  - function.ibase-pconnect.html: « ibasepconnect
  - function.ibase-query.html: ibasequery »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibaseprepare
---
# ibaseprepare

(PHP 5, PHP 7 < 7.4.0)

ibaseprepare — Підготовка запиту для подальшого зв'язування псевдозмінних та виконання

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

Підготовляє запит для подальшого зв'язування псевдозмінних та виконання (за допомогою [ibaseexecute()](function.ibase-execute.html)

### Список параметрів

`query`

Запит InterBase.

`link_identifier`

Ідентифікатор посилання InterBase, який повертається функцією [ibaseconnect()](function.ibase-connect.html). Якщо не вказано, передбачається останнє відкрите посилання.

`trans`

Дескриптор транзакції InterBase, з якою має бути пов'язаний запит. Якщо не вказано, передбачається транзакція стандартного з'єднання.

### Значення, що повертаються

Повертає дескриптор підготовленого запиту або **`false`** у разі виникнення помилки.
