---
navigation:
  - yac.info.md: '« Yac::info'
  - yac.setter.md: 'Yac::\_\_set »'
  - index.md: PHP Manual
  - class.yac.md: Yac
title: 'Yac::set'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yac::set

(PECL yac >= 1.0.0)

Yac::set — Зберігає у кеш

### Опис

```methodsynopsis
public Yac::set(string $keys, mixed $value, int $ttl = 0): bool
```

```methodsynopsis
public Yac::add(array $key_vals): bool
```

Додає елемент до кешу, якщо ключ уже існує, замінює його.

### Список параметрів

`keys`

Ключ (string)

`value`

Змішане значення. Можуть бути збережені всі типи значень php, крім [resource](language.types.resource.md)

`ttl`

Час життя

### Значення, що повертаються

Власне значення
