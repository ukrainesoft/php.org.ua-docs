Видаляє псевдонім сервера

-   [« EventHttp::construct](eventhttp.construct.html)
    
-   [EventHttp::setAllowedMethods »](eventhttp.setallowedmethods.html)
    
-   [PHP Manual](index.html)
    
-   [EventHttp](class.eventhttp.html)
    
-   Видаляє псевдонім сервера
    

# EventHttp::removeServerAlias

(PECL event >= 1.4.0-beta)

EventHttp::removeServerAlias ​​— Видаляє псевдонім сервера

### Опис

```methodsynopsis
public
   EventHttp::removeServerAlias(
    string
     $alias
   ): bool
```

Видаляє псевдонім сервера, доданий за допомогою [EventHttp::addServerAlias()](eventhttp.addserveralias.html)

### Список параметрів

`alias`

Псевдонім для видалення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventHttp::addServerAlias()](eventhttp.addserveralias.html) - Додає псевдонім сервера до об'єкта HTTP-сервера