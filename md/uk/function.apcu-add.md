---
navigation:
  - ref.apcu.md: « Функции APCu
  - function.apcu-cache-info.html: apcucacheinfo »
  - index.md: PHP Manual
  - ref.apcu.md: Функции APCu
title: apcuadd
---
# apcuadd

(PECL apcu >= 4.0.0)

apcuadd — Додати змінну до кешу

### Опис

```methodsynopsis
apcu_add(string $key, mixed $var, int $ttl = 0): bool
```

```methodsynopsis
apcu_add(array $values, mixed $unused = NULL, int $ttl = 0): array
```

Додає змінну в кеш, якщо її ще немає.

> **Зауваження**: На відміну від багатьох інших механізмів PHP, змінні, збережені **apcuadd()**, зберігаються між запитами, доки їх не видалять із кеша.

### Список параметрів

`key`

Ім'я, під яким буде збережено змінну. Значення `key` є унікальним для кеша, так що спроба використати **apcuadd()** для збереження змінної з ключем, що вже існує, не перезапише запис, а поверне **`false`**. (Це єдина різниця між **apcuadd()** і [apcustore()](function.apcu-store.html)

`var`

Змінна для збереження

`ttl`

Час життя; змінна `var` буде зберігатися протягом `ttl` секунд. Як тільки `ttl` секунд пройдуть, змінну буде видалено з кеша (при наступному запиті). Якщо параметр `ttl` не заданий (або `ttl` заданий як `0`), значення буде зберігатися доки не буде видалено явно, або з технічної причини (очищення кешу, перезапуск і т.д.)

`values`

Імена у ключах, змінні у значеннях.

### Значення, що повертаються

Повертає **`true`**, якщо вдалося занести значення в кеш, інакше повертає **`false`**. Другий тип синтаксису повертає масив із ключами, за якими сталася помилка.

### Приклади

**Приклад #1 Приклад використання **apcuadd()****

```php
<?php
$bar = 'BAR';
apcu_add('foo', $bar);
var_dump(apcu_fetch('foo'));
echo "\n";
$bar = 'NEVER GETS SET';
apcu_add('foo', $bar);
var_dump(apcu_fetch('foo'));
echo "\n";
?>
```

Результат виконання цього прикладу:

```
string(3) "BAR"
string(3) "BAR"
```

### Дивіться також

-   [apcustore()](function.apcu-store.html) - Кешує змінну
-   [apcufetch()](function.apcu-fetch.html) - Витягує з кеша збережену змінну
-   [apcudelete()](function.apcu-delete.html) - Видаляє збережене значення з кешу
