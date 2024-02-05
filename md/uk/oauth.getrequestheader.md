---
navigation:
  - oauth.getlastresponseinfo.md: '« OAuth::getLastResponseInfo'
  - oauth.getrequesttoken.md: 'OAuth::getRequestToken »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::getRequestHeader'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuth::getRequestHeader

(No version information available, might only be in Git)

OAuth::getRequestHeader — Згенерувати підпис заголовка OAuth

### Опис

```methodsynopsis
public OAuth::getRequestHeader(string $http_method, string $url, mixed $extra_parameters = ?): string|false
```

Генерує підпис заголовка OAuth на основі фінального методу HTTP, URL та додаткових параметрів.

### Список параметрів

`http_method`

HTTP метод.

`url`

URL-адреса запиту.

`extra_parameters`

Рядок або масив з додатковими параметрами.

### Значення, що повертаються

Рядок із заголовком запиту або \*\*`false`\*\*в случае возникновения ошибки
