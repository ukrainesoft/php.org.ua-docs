---
navigation:
  - function.dbase-close.md: « dbaseclose
  - function.dbase-delete-record.md: dbasedeleterecord »
  - index.md: PHP Manual
  - ref.dbase.md: dBase
title: dbasecreate
---
# dbasecreate

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbasecreate — Створює базу даних

### Опис

```methodsynopsis
dbase_create(string $path, array $fields, int $type = DBASE_TYPE_DBASE): resource
```

**dbasecreate()** створює базу даних dBase із заданими властивостями. Якщо файл вже існує, він не буде попередньо очищений. Для примусового очищення використовуйте функцію [dbasepack()](function.dbase-pack.md)

> **Зауваження**
> 
> На поведінку цієї функції впливає значення директиви [openbasedir](ini.core.md#ini.open-basedir)

### Список параметрів

`path`

Шлях до бази даних. Це може бути відносний або абсолютний шлях до файлу, де dBase буде зберігати ваші дані.

`fields`

Масив масивів, у якому кожен масив визначає формат одного поля бази даних. Формат кожного поля складається з імені цього поля, символу, що вказує тип поля, і, при необхідності, його довжину, точність та прапор обнулюваності. Типи файлів, що підтримуються, перераховані в [вступної секції](intro.dbase.md)

`type`

Тип створюваної бази даних. Або **`DBASE_TYPE_DBASE`** або **`DBASE_TYPE_FOXPRO`**

> **Зауваження**
> 
> Імена полів обмежені в довжину та не повинні перевищувати 10 символів.

### Значення, що повертаються

Повертає ресурс бази даних, якщо база даних успішно створена, або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| dbase 7.0.0 | Доданий параметр `type` |
| dbase 7.0.0 | Повертається тепер має тип resource а не int. |

### Приклади

**Приклад #1 Створення файлу бази даних dBase**

```php
<?php

// база данных "definition"
$def = array(
  array("date",     "D"),
  array("name",     "C",  50),
  array("age",      "N",   3, 0),
  array("email",    "C", 128),
  array("ismember", "L")
);

// создаём
if (!dbase_create('/tmp/test.dbf', $def)) {
  echo "Ошибка, не получается создать базу данных\n";
}

?>
```

### Дивіться також

-   [dbaseopen()](function.dbase-open.md) - Відкриває базу даних
-   [dbaseclose()](function.dbase-close.md) - Закриває базу даних
