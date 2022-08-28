Заборонити URL, використовуючи вираз VCL

-   [« VarnishAdmin::ban](varnishadmin.ban.html)
    
-   [VarnishAdmin::clearPanic »](varnishadmin.clearpanic.html)
    
-   [PHP Manual](index.html)
    
-   [VarnishAdmin](class.varnishadmin.html)
    
-   Заборонити URL, використовуючи вираз VCL
    

# VarnishAdmin::banUrl

(PECL varnish >= 0.3)

VarnishAdmin::banUrl — Заборонити URL-адресу, використовуючи вираз VCL

### Опис

```methodsynopsis
public VarnishAdmin::banUrl(string $vcl_regex): int
```

### Список параметрів

`vcl_regex`

Регулярний вираз URL у синтаксисі, сумісному з PCRE. Воно ґрунтується на команді varnish ban.

### Значення, що повертаються

Повертає статус команди Varnish.