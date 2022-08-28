Встановити дані програми (застарілий метод)

-   [« GearmanClient::setCreatedCallback](gearmanclient.setcreatedcallback.html)
    
-   [GearmanClient::setDataCallback »](gearmanclient.setdatacallback.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Встановити дані програми (застарілий метод)
    

# GearmanClient::setData

(PECL gearman <= 0.5.0)

GearmanClient::setData — Встановити дані програми (застарілий метод)

### Опис

```methodsynopsis
public GearmanClient::setData(string $data): bool
```

Встановлює деякі довільні дані додатки, які згодом можуть бути вилучені [GearmanClient::data()](gearmanclient.data.html)

> **Зауваження**
> 
> Цей метод було замінено на **GearmanCient::setContext()** у версії 0.6.0 модуля Gearman.

### Список параметрів

`data`

### Значення, що повертаються

Завжди повертає **`true`**

### Дивіться також

-   [GearmanClient::data()](gearmanclient.data.html) - Повертає дані програми (функція застаріла)