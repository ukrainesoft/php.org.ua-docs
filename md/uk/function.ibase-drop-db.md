---
navigation:
  - function.ibase-delete-user.md: « ibasedeleteuser
  - function.ibase-errcode.md: ibaseerrcode »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibasedropдб
---
# ibasedropдб

(PHP 5, PHP 7 < 7.4.0)

ibasedropdb — Видалення бази даних

### Опис

```methodsynopsis
ibase_drop_db(resource $connection = null): bool
```

Функція видаляє базу даних, яка була відкрита або за допомогою [ibaseconnect()](function.ibase-connect.md), або [ibasepconnect()](function.ibase-pconnect.md). База даних закривається та видаляється з сервера.

### Список параметрів

`connection`

Ідентифікатор посилання InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibaseconnect()](function.ibase-connect.md) - Відкриває з'єднання з базою даних
-   [ibasepconnect()](function.ibase-pconnect.md) - Відкриває постійне з'єднання з базою даних InterBase
