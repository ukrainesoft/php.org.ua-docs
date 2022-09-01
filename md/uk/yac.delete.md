---
navigation:
  - yac.construct.html: '« Yac::construct'
  - yac.dump.html: 'Yac::dump »'
  - index.html: PHP Manual
  - class.yac.html: Yac
title: 'Yac::delete'
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
