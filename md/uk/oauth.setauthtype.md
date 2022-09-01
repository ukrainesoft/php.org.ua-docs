---
navigation:
  - oauth.getrequesttoken.html: '« OAuth::getRequestToken'
  - oauth.setcapath.html: 'OAuth::setCAPath »'
  - index.html: PHP Manual
  - class.oauth.html: OAuth
title: 'OAuth::setAuthType'
---
# OAuth::setAuthType

(PECL OAuth >= 0.99.1)

OAuth::setAuthType — Встановити тип авторизації

### Опис

```methodsynopsis
public OAuth::setAuthType(int $auth_type): bool
```

Встановлює, як повинні передаватися параметри OAuth.

### Список параметрів

`auth_type`

`auth_type` може бути заданий одним з наступних прапорів (у порядку зменшення переваги згідно з розділом 5.2 OAuth 1.0):

**`OAUTH_AUTH_TYPE_AUTHORIZATION`**

Передавати параметри OAuth HTTP-заголовку `Authorization`

**`OAUTH_AUTH_TYPE_FORM`**

Додати параметри OAuth у тіло запиту HTTP POST.

**`OAUTH_AUTH_TYPE_URI`**

Додати параметри OAuth до URI запиту.

**`OAUTH_AUTH_TYPE_NONE`**

Чи не передавати.

### Значення, що повертаються

Повертає **`true`** або **`false`** (наприклад, якщо параметр `auth_type` заданий некоректно.)

### список змін

| Версия | Описание |
| --- | --- |
| PECL oauth 1.0.0 | Раніше у разі виникнення помилки повертався **`null`** замість **`false`** |
