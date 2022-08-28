Витягує значення з кешу

-   [« Yac::flush](yac.flush.html)
    
-   [Yac::\_\_get »](yac.getter.html)
    
-   [PHP Manual](index.html)
    
-   [Yac](class.yac.html)
    
-   Витягує значення з кешу
    

# Yac::get

(PECL yac >= 1.0.0)

Yac::get — Витягує значення з кешу

### Опис

```methodsynopsis
public Yac::get(string|array $key, int &$cas = null): mixed
```

Витягує значення з кешу

### Список параметрів

`key`

Ключ (string) або масив (array), що складається з кількох ключів

`cas`

Якщо не **`null`**, буде встановлено регістр вилучених елементів.

### Значення, що повертаються

Змішане значення у разі успішного виконання, false у разі виникнення помилки