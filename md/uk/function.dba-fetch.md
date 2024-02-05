---
navigation:
  - function.dba-exists.md: « dba\_exists
  - function.dba-firstkey.md: dba\_firstkey »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dba\_fetch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dba\_fetch

(PHP 4, PHP 5, PHP 7, PHP 8)

dba\_fetch — Витягує дані за вказаним ключем

### Опис

```methodsynopsis
dba_fetch(string|array $key, resource $dba, int $skip = 0): string|false
```

Перевантажена сигнатура застаріла з PHP 8.3.0:

```methodsynopsis
dba_fetch(string|array $key, int $skip, resource $dba): string
```

**dba\_fetch()** витягує дані з бази даних, заданої `dba`, визначені ключем `key`

### Список параметрів

`key`

Ключ, для якого треба отримати дані.

> **Зауваження** :
> 
> Коли працює з ini-файлом, ця функція приймає масив як ключ, де за індексом 0 задана група, а за індексом 1 - ім'я параметра. Додатково дивіться [dba\_key\_split()](function.dba-key-split.md)

`dba`

Обробник бази даних, повернутий [dba\_open()](function.dba-open.md) або [dba\_popen()](function.dba-popen.md)

`skip`

Число пар ключ-значення, які потрібно проігнорувати під час роботи з базою даних cdb. Цей параметр ігнорується при роботі з іншими базами даних, в яких не підтримуються множинні ключі з однаковим ім'ям.

### Значення, що повертаються

Повертає рядок, якщо пара ключ/дані знайдена, інакше повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Виклик функції \*\*dba\_fetch()\*\*с параметром`dba` як третій аргумент застарів. |
| 8.2.0 | Необов'язковий параметр skip функції **dba\_fetch()** тепер знаходиться в кінці відповідно до користувальницької семантики PHP; перевантажена сигнатура, як і раніше, приймається, але не рекомендується. |

### Дивіться також

-   [dba\_exists()](function.dba-exists.md) \- Перевіряє, чи існує ключ
-   [dba\_delete()](function.dba-delete.md) \- Видаляє запис бази даних, визначену ключем
-   [dba\_insert()](function.dba-insert.md) \- Вставляє запис
-   [dba\_replace()](function.dba-replace.md) \- Перезаписати або вставити запис
-   [dba\_key\_split()](function.dba-key-split.md) \- Розділяє ключ, заданий у вигляді рядка та створює масив з отриманих частин
