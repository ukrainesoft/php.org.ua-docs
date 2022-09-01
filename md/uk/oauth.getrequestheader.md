---
navigation:
  - oauth.getlastresponseinfo.html: '« OAuth::getLastResponseInfo'
  - oauth.getrequesttoken.html: 'OAuth::getRequestToken »'
  - index.html: PHP Manual
  - class.oauth.html: OAuth
title: 'OAuth::getRequestHeader'
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

Рядок із заголовком запиту або **`false`** у разі виникнення помилки
