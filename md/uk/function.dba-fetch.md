Витягує дані за вказаним ключем

-   [« dbaexists](function.dba-exists.html)
    
-   [dbafirstkey »](function.dba-firstkey.html)
    
-   [PHP Manual](index.md)
    
-   [Функції DBA](ref.dba.md)
    
-   Витягує дані за вказаним ключем
    

# dbafetch

(PHP 4, PHP 5, PHP 7, PHP 8)

dbafetch — Витягує дані за вказаним ключем

### Опис

```methodsynopsis
dba_fetch(string $key, resource $handle): string
```

```methodsynopsis
dba_fetch(string $key, int $skip, resource $handle): string
```

**dbafetch()** витягує дані з бази даних, заданої `handle`, визначені ключем `key`

### Список параметрів

`key`

Ключ, для якого треба отримати дані.

> **Зауваження**
> 
> Коли працює з ini-файлом, ця функція приймає масив як ключ, де за індексом 0 задана група, а за індексом 1 - ім'я параметра. Додатково дивіться [dbakeysplit()](function.dba-key-split.html)

`skip`

Число пар ключ-значення, які потрібно проігнорувати під час роботи з базою даних cdb. Цей параметр ігнорується при роботі з іншими базами даних, в яких не підтримуються множинні ключі з однаковим ім'ям.

`handle`

Обробник бази даних, повернутий [dbaopen()](function.dba-open.html) або [dbapopen()](function.dba-popen.html)

### Значення, що повертаються

Повертає рядок, якщо пара ключ/дані знайдена, інакше повертає **`false`**

### Дивіться також

-   [dbaexists()](function.dba-exists.html) - Перевіряє, чи існує ключ
-   [dbadelete()](function.dba-delete.html) - Видаляє запис бази даних, визначену ключем
-   [dbainsert()](function.dba-insert.html) - Вставляє запис
-   [dbareplace()](function.dba-replace.html) - Перезаписати або вставити запис
-   [dbakeysplit()](function.dba-key-split.html) - Розділяє ключ, заданий у вигляді рядка та створює масив з отриманих частин