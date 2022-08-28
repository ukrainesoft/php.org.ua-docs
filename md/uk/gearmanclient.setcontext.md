Встановити контекст програми

-   [« GearmanClient::setCompleteCallback](gearmanclient.setcompletecallback.html)
    
-   [GearmanClient::setCreatedCallback »](gearmanclient.setcreatedcallback.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Встановити контекст програми
    

# GearmanClient::setContext

(PECL gearman >= 0.6.0)

GearmanClient::setContext — Встановити контекст програми

### Опис

```methodsynopsis
public GearmanClient::setContext(string $context): bool
```

Встановлює довільний рядок для надання контексту програми, яка може бути пізніше отримана за допомогою [GearmanClient::context()](gearmanclient.context.html)

### Список параметрів

`context`

Довільні дані контексту

### Значення, що повертаються

Завжди повертає **`true`**

### Дивіться також

-   [GearmanClient::context()](gearmanclient.context.html) - Повертає контекст програми