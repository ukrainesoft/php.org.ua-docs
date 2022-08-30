Перевести подію в пасивний стан

-   [« Event::construct](event.construct.html)
    
-   [Event::delSignal »](event.delsignal.html)
    
-   [PHP Manual](index.html)
    
-   [Event](class.event.html)
    
-   Перевести подію в пасивний стан
    

# Event::del

(PECL event >= 1.2.6-beta)

Event::del — Перевести подію в пасивний стан

### Опис

```methodsynopsis
public
   Event::del(): bool
```

Видаляє подію з набору подій, що відстежуються, тобто. переводить їх у стан не-ожидания.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [Event::add()](event.add.html) - Перевести подію у стан очікування