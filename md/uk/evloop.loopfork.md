Викликається після розгалуження

-   [« EvLoop::io](evloop.io.html)
    
-   [EvLoop::now »](evloop.now.html)
    
-   [PHP Manual](index.html)
    
-   [EvLoop](class.evloop.html)
    
-   Викликається після розгалуження
    

# EvLoop::loopFork

(PECL ev >= 0.2.0)

UvLoop::loop Fork — Викликається після розгалуження

### Опис

```methodsynopsis
public
   EvLoop::loopFork(): void
```

Повинен викликатися після *розгалуження* у дочірньому елементі перед входом або продовженням циклу подій. Альтернативою є використання **`Ev::FLAG_FORKCHECK`**, яка викликає цю функцію автоматично при певній втраті продуктивності (див. [» документацию libev](http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#FUNCTIONS_CONTROLLING_EVENT_LOOPS)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.