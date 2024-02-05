---
navigation:
  - function.dbase-close.md: « dbase\_close
  - function.dbase-delete-record.md: dbase\_delete\_record »
  - index.md: PHP Manual
  - ref.dbase.md: dBase
title: dbase\_create
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dbase\_create

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbase\_create — Створює базу даних

### Опис

```methodsynopsis
dbase_create(string $path, array $fields, int $type = DBASE_TYPE_DBASE): resource
```

**dbase\_create()** створює базу даних dBase із заданими властивостями. Якщо файл вже існує, він не буде попередньо очищений. Для примусового очищення використовуйте функцію [dbase\_pack()](function.dbase-pack.md)

> **Зауваження** :
> 
> На поведінку цієї функції впливає значення директиви [open\_basedir](ini.core.md#ini.open-basedir)

### Список параметрів

`path`

Шлях до бази даних. Це може бути відносний або абсолютний шлях до файлу, де dBase буде зберігати ваші дані.

`fields`

Масив масивів, у якому кожен масив визначає формат одного поля бази даних. Формат кожного поля складається з імені цього поля, символу, що вказує тип поля, і, при необхідності, його довжину, точність та прапор обнулюваності. Типи файлів, що підтримуються, перераховані в [вступної секції](intro.dbase.md)

`type`

Тип створюваної бази даних. Або **`DBASE_TYPE_DBASE`**либо**`DBASE_TYPE_FOXPRO`**

> **Зауваження** :
> 
> Імена полів обмежені в довжину та не повинні перевищувати 10 символів.

### Значення, що повертаються

Повертає ресурс бази даних, якщо база даних успішно створена, або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| dbase 7.0.0 | Добавлен параметр`type` |
| dbase 7.0.0 | Повертається тепер має тип resource а не int. |

### Приклади

**Приклад #1 Створення файлу бази даних dBase**

```php
<?php

// база данных "definition"
$def = array(
  array("date",     "D"),
  array("name",     "C",  50),
  array("age",      "N",   3, 0),
  array("email",    "C", 128),
  array("ismember", "L")
);

// создаём
if (!dbase_create('/tmp/test.dbf', $def)) {
  echo "Ошибка, не получается создать базу данных\n";
}

?>
```

### Дивіться також

-   [dbase\_open()](function.dbase-open.md) \- Відкриває базу даних
-   [dbase\_close()](function.dbase-close.md) \- Закриває базу даних
