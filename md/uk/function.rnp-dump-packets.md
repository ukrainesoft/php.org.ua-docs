---
navigation:
  - function.rnp-dump-packets-to-json.md: « rnp\_dump\_packets\_to\_json
  - function.rnp-ffi-create.md: rnp\_ffi\_create »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_dump\_packets
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_dump\_packets

(PECL rnp >= 0.1.1)

rnp\_dump\_packets — Вивантажує інформацію про потік пакетів OpenPGP у людино-читаному форматі

### Опис

```methodsynopsis
rnp_dump_packets(string $input, int $flags): string|false
```

### Список параметрів

`input`

Вхідний рядок, який містить дані OpenPGP у двійковому або ASCII-закодованому форматі.

`flags`

Дивіться певні константи **`RNP_JSON_DUMP_*`**

### Значення, що повертаються

Текст, що описує послідовність пакетів або \*\*`false`\*\*в случае возникновения ошибки.
