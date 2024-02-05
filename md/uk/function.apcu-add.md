---
navigation:
  - ref.apcu.md: « Функції APCu
  - function.apcu-cache-info.md: apcu\_cache\_info »
  - index.md: PHP Manual
  - ref.apcu.md: Функції APCu
title: apcu\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apcu\_add

(PECL apcu >= 4.0.0)

apcu\_add — Додати змінну до кешу

### Опис

```methodsynopsis
apcu_add(string $key, mixed $var, int $ttl = 0): bool
```

```methodsynopsis
apcu_add(array $values, mixed $unused = NULL, int $ttl = 0): array
```

Додає змінну в кеш, якщо її ще немає.

> **Зауваження**: На відміну від багатьох інших механізмів PHP, змінні, збережені **apcu\_add()**, зберігаються між запитами, доки їх не видалять із кеша.

### Список параметрів

`key`

Ім'я, під яким буде збережено змінну. Значення `key` є унікальним для кешу, так що спроба використати **apcu\_add()** для збереження змінної з ключем, що вже існує, не перезапише запис, а поверне **`false`**. (Це єдина різниця між \*\*apcu\_add()\*\*и[apcu\_store()](function.apcu-store.md)

`var`

Змінна для збереження

`ttl`

Время жизни; переменная`var` буде зберігатися протягом `ttl` секунд. Як тільки `ttl`секунд пройдут, переменная будет удалена из кеша (при следующем запросе). Если параметр`ttl`не задан (или`ttl`задан как ), значення буде зберігатися доки не буде видалено явно, або з технічної причини (очищення кешу, перезапуск і т.д.)

`values`

Імена у ключах, змінні у значеннях.

### Значення, що повертаються

Повертає **`true`**, якщо вдалося занести значення в кеш, інакше повертає **`false`**. Другий тип синтаксису повертає масив із ключами, за якими сталася помилка.

### Приклади

**Приклад #1 Приклад використання** apcu\_add()\*\*\*\*

```php
<?php
$bar = 'BAR';
apcu_add('foo', $bar);
var_dump(apcu_fetch('foo'));
echo "\n";
$bar = 'NEVER GETS SET';
apcu_add('foo', $bar);
var_dump(apcu_fetch('foo'));
echo "\n";
?>
```

Результат виконання наведеного прикладу:

```
string(3) "BAR"
string(3) "BAR"
```

### Дивіться також

-   [apcu\_store()](function.apcu-store.md) \- Кешує змінну
-   [apcu\_fetch()](function.apcu-fetch.md) \- Витягує з кеша збережену змінну
-   [apcu\_delete()](function.apcu-delete.md) \- Видаляє збережене значення з кешу
