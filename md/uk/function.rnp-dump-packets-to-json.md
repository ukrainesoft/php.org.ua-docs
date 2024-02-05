---
navigation:
  - function.rnp-decrypt.md: « rnp\_decrypt
  - function.rnp-dump-packets.md: rnp\_dump\_packets »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_dump\_packets\_to\_json
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_dump\_packets\_to\_json

(PECL rnp >= 0.1.1)

rnp\_dump\_packets\_to\_json — Вивантаження інформації про потік пакетів OpenPGP у рядок JSON

### Опис

```methodsynopsis
rnp_dump_packets_to_json(string $input, int $flags): string|false
```

### Список параметрів

`input`

Вхідний рядок, який містить дані OpenPGP у двійковому або ASCII-закодованому форматі.

`flags`

Дивіться певні константи **`RNP_JSON_DUMP_*`**

### Значення, що повертаються

Рядок JSON з виводом або \*\*`false`\*\*в случае возникновения ошибки.
