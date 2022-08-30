Конструктор класу Patch

-   [« ComponerePatch](class.componere-patch.html)
    
-   [ComponerePatch::apply »](componere-patch.apply.html)
    
-   [PHP Manual](index.html)
    
-   [ComponerePatch](class.componere-patch.html)
    
-   Конструктор класу Patch
    

# ComponerePatch::construct

(Componere 2 >= 2.1.0)

ComponerePatch::construct - Конструктор класу Patch

### Опис

public **ComponerePatch::construct**(object `$instance`

public **ComponerePatch::construct**(object `$instance`, array `$interfaces`

### Список параметрів

`instance`

Призначення для цього патчу

`interfaces`

Реєстронезалежний масив імен класів

### Винятки

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.html)якщо клас не може бути знайдений `interfaces`

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.html), якщо клас у `interfaces` не є інтерфейсом