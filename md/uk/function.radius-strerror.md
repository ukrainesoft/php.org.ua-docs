Повертає повідомлення про помилку

-   [« radius\_server\_secret](function.radius-server-secret.html)
    
-   [Модули для работы с командной строкой »](refs.utilspec.cmdline.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Radius](ref.radius.html)
    
-   Повертає повідомлення про помилку
    

# radiusstrerror

(PECL radius >= 1.1.0)

radiusstrerror — Повертає повідомлення про помилку

### Опис

```methodsynopsis
radius_strerror(resource $radius_handle): string
```

У разі помилки функцій radius, вони записують повідомлення про помилку. Це повідомлення можна отримати за допомогою цієї функції.

### Список параметрів

`radius_handle`

Ресурс RADIUS

### Значення, що повертаються

Повертає повідомлення про помилки у вигляді рядка з функцій radius, що завершилися помилкою.