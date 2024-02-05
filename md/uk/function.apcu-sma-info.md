---
navigation:
  - function.apcu-key-info.md: « apcu\_key\_info
  - function.apcu-store.md: apcu\_store »
  - index.md: PHP Manual
  - ref.apcu.md: Функції APCu
title: apcu\_sma\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apcu\_sma\_info

(PECL apcu >= 4.0.0)

apcu\_sma\_info — Витягує інформацію про виділення пам'яті APCu, що розділяється.

### Опис

```methodsynopsis
apcu_sma_info(bool $limited = false): array|false
```

Витягує інформацію про виділення пам'яті APCu.

### Список параметрів

`limited`

Если установлен в\*\*`false`\*\*(по умолчанию),**apcu\_sma\_info()** поверне детальну інформацію про кожен сегмент.

### Значення, що повертаються

Масив даних про виділену пам'ять, що розділяється; \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** apcu\_sma\_info()\*\*\*\*

```php
<?php
print_r(apcu_sma_info());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [num_seg] => 1
    [seg_size] => 31457280
    [avail_mem] => 31448408
    [block_lists] => Array
        (
            [0] => Array
                (
                    [0] => Array
                        (
                            [size] => 31448408
                            [offset] => 8864
                        )

                )

        )

)
```

### Дивіться також

-   [Директиви конфігурації APCu](apcu.configuration.md)
