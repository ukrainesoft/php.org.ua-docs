Закриває Stomp-з'єднання

-   [« Stomp::construct](stomp.construct.md)
    
-   [Stomp::error »](stomp.error.md)
    
-   [PHP Manual](index.md)
    
-   [Stomp](class.stomp.md)
    
-   Закриває Stomp-з'єднання
    

# Stomp::destruct

# stompclose

(PECL stomp >= 0.1.0)

Stomp::destruct - stompclose - Закриває Stomp-з'єднання

### Опис

Об'єктно-орієнтований стиль (деструктор):

public **Stomp::destruct**

Процедурний стиль:

```methodsynopsis
stomp_close(resource $link): bool
```

Закриває відкриті раніше з'єднання.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stompconnect()](stomp.construct.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

Дивіться [stompconnect()](stomp.construct.md)