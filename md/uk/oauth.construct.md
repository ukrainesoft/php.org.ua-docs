---
navigation:
  - class.oauth.md: « OAuth
  - oauth.destruct.md: 'OAuth::\_\_destruct »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuth::\_\_construct

(PECL OAuth >= 0.99.1)

OAuth::\_\_construct — Створює новий об'єкт OAuth

### Опис

public **OAuth::\_\_construct**  
string`$consumer_key`,  
string`$consumer_secret`,  
string`$signature_method` **`OAUTH_SIG_METHOD_HMACSHA1`**,  
int`$auth_type`  
) .

Створює новий об'єкт OAuth

### Список параметрів

`consumer_key`

Ключ споживача наданий сервіс провайдером.

`consumer_secret`

Секрет споживача наданий сервіс провайдером.

`signature_method`

Цей параметр необов'язково визначає, який метод підпису буде використаний. За замовчуванням використовується **`OAUTH_SIG_METHOD_HMACSHA1`**(HMAC-SHA1).

`auth_type`

Цей необов'язковий параметр визначає, як передавати параметри OAuth споживачеві. За замовчуванням використовується **`OAUTH_AUTH_TYPE_AUTHORIZATION`** (У заголовку `Authorization`
