Видаляє елементи з кешу

-   [« Yac::\_\_construct](yac.construct.html)
    
-   [Yac::dump »](yac.dump.html)
    
-   [PHP Manual](index.html)
    
-   [Yac](class.yac.html)
    
-   Видаляє елементи з кешу
    

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