---
navigation:
  - function.hash-file.md: « hashfile
  - function.hash-hkdf.md: hashhkdf »
  - index.md: PHP Manual
  - ref.hash.md: Функции Hash
title: hashfinal
---
# hashfinal

(PHP 5> = 5.1.2, PHP 7, PHP 8, PECL hash> = 1.1)

hashfinal — Завершує інкрементальне хешування та повертає результат у вигляді хеш-коду

### Опис

```methodsynopsis
hash_final(HashContext $context, bool $binary = false): string
```

### Список параметрів

`context`

Контекст хешування, повернутий [hashinit()](function.hash-init.md)

`binary`

Коли встановлено в **`true`**, виводить необроблені двійкові дані При **`false`** виводить дані у шістнадцятковому кодуванні в нижньому регістрі.

### Значення, що повертаються

Повертає рядок, що містить обчислений хеш-код у шістнадцятковому кодуванні в нижньому регістрі. Якщо `binary` заданий як **`true`**, то повертається хеш-код у вигляді бінарних даних.

### список змін

| Версия | Описание |
| --- | --- |
|  | Приймає [HashContext](class.hashcontext.md), а чи не ресурс. |

### Приклади

**Приклад #1 Приклад використання **hashfinal()****

```php
<?php
$ctx = hash_init('sha1');
hash_update($ctx, 'Наглый коричневый лисёнок прыгает вокруг ленивой собаки.');
echo hash_final($ctx);
?>
```

Результат виконання цього прикладу:

```
dc495843a3a90b46c12e254102599571fa83a737
```

### Дивіться також

-   [hashinit()](function.hash-init.md) - Ініціалізація інкрементального контексту хешування
-   [hashupdate()](function.hash-update.md) - Додає дані до активного контексту хешування
-   [hashupdatestream()](function.hash-update-stream.md) - Додає дані з відкритого потоку до активного контексту хешування
-   [hashupdatefile()](function.hash-update-file.md) - Додає дані з файлу до активного контексту хешування
