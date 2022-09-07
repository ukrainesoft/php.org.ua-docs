---
navigation:
  - class.yac.md: « Yac
  - yac.construct.md: 'Yac::construct »'
  - index.md: PHP Manual
  - class.yac.md: Yac
title: 'Yac::add'
---
# Yac::add

(PECL yac >= 1.0.0)

Yac::add — Зберігає у кеш

### Опис

```methodsynopsis
public Yac::add(string $keys, mixed $value, int $ttl = 0): bool
```

```methodsynopsis
public Yac::add(array $key_vals): bool
```

Додає елемент у кеш.

### Список параметрів

`keys`

Ключ (string)

`value`

Змішане значення. Можуть бути збережені всі типи значень php, крім [resource](language.types.resource.md)

`ttl`

Час життя

### Значення, що повертаються

bool, **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки

> **Зауваження**
> 
> **Yac::add()** може завершитися з помилкою, якщо не вдалося отримати блокування cas, тому, якщо вам потрібно, щоб значення зберігалося належним чином, ви можете написати таке:
> 
> **Приклад #1 Переконайтеся, що елемент зберігається**
> 
> ```php
> while(!$yac->set("key", "vale));
> ```
