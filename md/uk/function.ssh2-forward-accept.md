Приймає з'єднання, створене слухачем

-   [« ssh2\_fingerprint](function.ssh2-fingerprint.html)
    
-   [ssh2\_forward\_listen »](function.ssh2-forward-listen.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SSH2](ref.ssh2.html)
    
-   Приймає з'єднання, створене слухачем
    

# ssh2forwardaccept

(PECL ssh2> = 0.9.0)

ssh2forwardaccept — Приймає з'єднання, створене слухачем

### Опис

```methodsynopsis
ssh2_forward_accept(resource $listener): resource|false
```

Приймає з'єднання, створене слухачем.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`desc`

Ресурс SSH2 Listener, отриманий у результаті виклику [ssh2\_forward\_listen()](function.ssh2-forward-listen.html)

### Значення, що повертаються

Повертає ресурс потоку або **`false`** у разі виникнення помилки.