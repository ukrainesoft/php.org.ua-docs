Зберігає у кеш

-   [« Yac::info](yac.info.md)
    
-   [Yac::set »](yac.setter.md)
    
-   [PHP Manual](index.md)
    
-   [Yac](class.yac.md)
    
-   Зберігає у кеш
    

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