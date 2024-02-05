---
navigation:
  - yac.construct.md: '« Yac::\_\_construct'
  - yac.dump.md: 'Yac::dump »'
  - index.md: PHP Manual
  - class.yac.md: Yac
title: 'Yac::delete'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yac::delete

(PECL yac >= 1.0.0)

Yac::delete — Видаляє елементи з кешу

### Опис

```methodsynopsis
public Yac::delete(string|array $keys, int $ttl = ?): bool
```

Видаляє елементи з кешу

### Список параметрів

`keys`

Рядковий ключ або масив з декількох ключів, які потрібно видалити

`ttl`

Якщо встановлено затримку, видалення позначить елементи як неприпустимі протягом ttl секунд.

### Значення, що повертаються
