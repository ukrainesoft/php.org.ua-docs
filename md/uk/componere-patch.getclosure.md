Отримує замикання

-   [« ComponerePatch::derive](componere-patch.derive.html)
    
-   [ComponerePatch::getClosures »](componere-patch.getclosures.html)
    
-   [PHP Manual](index.html)
    
-   [ComponerePatch](class.componere-patch.html)
    
-   Отримує замикання
    

# ComponerePatch::getClosure

(Componere 2 >= 2.1.0)

ComponerePatch::getClosure — Отримує замикання

### Опис

```methodsynopsis
public Componere\Patch::getClosure(string $name): Closure
```

Повинен повернути замикання для вказаного методу

### Список параметрів

`name`

Реєстронезалежне ім'я методу

### Значення, що повертаються

Замикання, прив'язане до правильної області та об'єкту

### Винятки

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.html) якщо `name` НЕ знайдений