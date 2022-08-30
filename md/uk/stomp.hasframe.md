Перевіряє, чи можливе читання кадру

-   [« Stomp::getSessionId](stomp.getsessionid.html)
    
-   [Stomp::readFrame »](stomp.readframe.html)
    
-   [PHP Manual](index.html)
    
-   [Stomp](class.stomp.html)
    
-   Перевіряє, чи можливе читання кадру
    

# Stomp::hasFrame

# stomphasframe

(PECL stomp >= 0.1.0)

Stomp::hasFrame -- stomphasframe — Перевіряє, чи можливо читати кадр

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Stomp::hasFrame(): bool
```

Процедурний стиль:

```methodsynopsis
stomp_has_frame(resource $link): bool
```

Перевіряє, чи можливо читати кадр.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stompconnect()](stomp.construct.html)

### Значення, що повертаються

Повертає **`true`** якщо кадр можна прочитати, інакше **`false`**