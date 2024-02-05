---
navigation:
  - function.hash-file.md: « hash\_file
  - function.hash-hkdf.md: hash\_hkdf »
  - index.md: PHP Manual
  - ref.hash.md: Функції Hash
title: hash\_final
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# hash\_final

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL hash >= 1.1)

hash\_final — Завершує інкрементальне хешування та повертає результат у вигляді хеш-коду

### Опис

```methodsynopsis
hash_final(HashContext $context, bool $binary = false): string
```

### Список параметрів

`context`

Контекст хешування, повернутий [hash\_init()](function.hash-init.md)

`binary`

Когда установлено в\*\*`true`\*\*, виводить необроблені двійкові дані При **`false`** виводить дані у шістнадцятковому кодуванні в нижньому регістрі.

### Значення, що повертаються

Повертає рядок, що містить обчислений хеш-код у шістнадцятковому кодуванні в нижньому регістрі. Якщо `binary`задан как\*\*`true`\*\*, то повертається хеш-код у вигляді бінарних даних.

### список змін

| Версия | Опис |
| --- | --- |
| 7.2.0 | Приймає [HashContext](class.hashcontext.md), а чи не ресурс. |

### Дивіться також

-   [hash\_init()](function.hash-init.md) \- Ініціалізація інкрементального контексту хешування
-   [hash\_update()](function.hash-update.md) \- Додає дані до активного контексту хешування
-   [hash\_update\_stream()](function.hash-update-stream.md) \- Додає дані з відкритого потоку до активного контексту хешування
-   [hash\_update\_file()](function.hash-update-file.md) \- Додає дані з файлу до активного контексту хешування
