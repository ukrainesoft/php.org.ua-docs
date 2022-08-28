Отримує замикання

-   [« Componere\\Definition::getClosure](componere-definition.getclosure.html)
    
-   [Componere\\Patch »](class.componere-patch.html)
    
-   [PHP Manual](index.html)
    
-   [Componere\\Definition](class.componere-definition.html)
    
-   Отримує замикання
    

# ComponereDefinition::getClosures

(Componere 2 >= 2.1.0)

ComponereDefinition::getClosures — Отримує замикання

### Опис

```methodsynopsis
public Componere\Definition::getClosures(): array
```

Повертає масив замикань

### Значення, що повертаються

Повертає всі методи у вигляді масиву об'єктів Closure, прив'язаних до коректної області

### Винятки

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.html), якщо Definition вже було зареєстровано