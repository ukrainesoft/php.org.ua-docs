---
navigation:
  - function.shmop-close.md: « shmop\_close
  - function.shmop-open.md: shmop\_open »
  - index.md: PHP Manual
  - ref.shmop.md: 'Пам''ять, що розділяється (shared)'
title: shmop\_delete
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# shmop\_delete

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

shmop\_delete — Видалення блоку пам'яті, що розділяється.

### Опис

```methodsynopsis
shmop_delete(Shmop $shmop): bool
```

**shmop\_delete()** використовується для видалення блоку пам'яті, що розділяється.

### Список параметрів

`shmop`

Ресурс блоку пам'яті, що повертається функцією [shmop\_open()](function.shmop-open.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`shmop` чекає на екземпляр [Shmop](class.shmop.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Видалення блоку пам'яті, що розділяється**

```php
<?php
shmop_delete($shm_id);
?>
```

У наведеному прикладі показано видалення блоку пам'яті, що розділяється, що має ідентифікатор `$shm_id`
