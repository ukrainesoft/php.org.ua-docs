Отримання патчу

-   [« ComponerePatch::isApplied](componere-patch.isapplied.html)
    
-   [ComponerePatch::getClosure »](componere-patch.getclosure.html)
    
-   [PHP Manual](index.html)
    
-   [ComponerePatch](class.componere-patch.html)
    
-   Отримання патчу
    

# ComponerePatch::derive

(Componere 2 >= 2.1.1)

ComponerePatch::derive — Отримання патчу

### Опис

```methodsynopsis
public Componere\Patch::derive(object $instance): Patch
```

Повинен отримати Patch для заданого екземпляра `instance`

### Список параметрів

`instance`

Призначення для отриманого патчу

### Значення, що повертаються

Patch для `instance` виходить з поточного Patch

### Винятки

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.html) якщо `instance` не сумісний