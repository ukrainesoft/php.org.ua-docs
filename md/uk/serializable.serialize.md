Представляє об'єкт у вигляді рядка

-   [« Serializable](class.serializable.html)
    
-   [Serializable::unserialize »](serializable.unserialize.html)
    
-   [PHP Manual](index.html)
    
-   [Serializable](class.serializable.html)
    
-   Представляє об'єкт у вигляді рядка
    

# Serializable::serialize

(PHP 5> = 5.1.0, PHP 7, PHP 8)

Serializable::serialize — Представляє об'єкт у вигляді рядка

### Опис

```methodsynopsis
public Serializable::serialize(): ?string
```

Повертає рядкову виставу об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядкову виставу об'єкта або **`null`**

### Помилки

Викидає виняток [Exception](class.exception.html) при поверненні типів, відмінних від рядка або **`null`**

### Дивіться також

-   [sleep()](language.oop5.magic.html#object.sleep)
-   [serialize()](language.oop5.magic.html#object.serialize)