Згенерувати підпис

-   [« OAuth::fetch](oauth.fetch.html)
    
-   [OAuth::getAccessToken »](oauth.getaccesstoken.html)
    
-   [PHP Manual](index.html)
    
-   [OAuth](class.oauth.html)
    
-   Згенерувати підпис
    

# OAuth::generateSignature

(No version information available, might only be in Git)

OAuth::generateSignature — Згенерувати підпис

### Опис

```methodsynopsis
public OAuth::generateSignature(string $http_method, string $url, mixed $extra_parameters = ?): string|false
```

Генерує підпис на основі методу HTTP, URL та додаткових параметрів.

### Список параметрів

`http_method`

HTTP-метод для запиту

`url`

URL запиту

`extra_parameters`

Рядок або масив додаткових параметрів.

### Значення, що повертаються

Рядок з підписом або **`false`** у разі виникнення помилки