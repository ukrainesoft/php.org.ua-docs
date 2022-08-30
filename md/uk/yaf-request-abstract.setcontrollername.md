Встановлює ім'я контролера

-   [« YafRequestAbstract::setBaseUri](yaf-request-abstract.setbaseuri.html)
    
-   [YafRequestAbstract::setDispatched »](yaf-request-abstract.setdispatched.html)
    
-   [PHP Manual](index.md)
    
-   [YafRequestAbstract](class.yaf-request-abstract.html)
    
-   Встановлює ім'я контролера
    

# YafRequestAbstract::setControllerName

(Yaf >=1.0.0)

YafRequestAbstract::setControllerName — Встановлює ім'я контролера

### Опис

```methodsynopsis
public Yaf_Request_Abstract::setControllerName(string $controller, bool $format_name = true): void
```

Встановлює ім'я контролера для запиту, зазвичай використовується маршрутизатором для встановлення імені контролера результату маршруту.

### Список параметрів

`controller`

string, ім'я контролера, має бути в CamelCase, наприклад, "Index" або "FooBar"

`format_name`

Додано в Yaf 3.2.0, за умовчанням Yaf відформатує ім'я CamelCase, якщо для нього встановлено значення **`false`**, Yaf установить оригінальне ім'я для запиту.

### Значення, що повертаються