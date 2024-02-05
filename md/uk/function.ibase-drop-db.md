---
navigation:
  - function.ibase-delete-user.md: « ibase\_delete\_user
  - function.ibase-errcode.md: ibase\_errcode »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_drop\_db
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_drop\_db

(PHP 5, PHP 7 < 7.4.0)

ibase\_drop\_db — Видалення бази даних

### Опис

```methodsynopsis
ibase_drop_db(resource $connection = null): bool
```

Функція видаляє базу даних, яка була відкрита або за допомогою [ibase\_connect()](function.ibase-connect.md), либо[ibase\_pconnect()](function.ibase-pconnect.md). База даних закривається та видаляється з сервера.

### Список параметрів

`connection`

Ідентифікатор посилання InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ibase\_connect()](function.ibase-connect.md) \- Відкриває з'єднання з базою даних
-   [ibase\_pconnect()](function.ibase-pconnect.md) \- Відкриває постійне з'єднання з базою даних InterBase
