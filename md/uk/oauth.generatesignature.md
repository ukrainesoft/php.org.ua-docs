---
navigation:
  - oauth.fetch.md: '« OAuth::fetch'
  - oauth.getaccesstoken.md: 'OAuth::getAccessToken »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::generateSignature'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Строка с подписью или\*\*`false`\*\*в случае возникновения ошибки
