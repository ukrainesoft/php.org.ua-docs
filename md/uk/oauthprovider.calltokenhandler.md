---
navigation:
  - oauthprovider.calltimestampnoncehandler.md: '« OAuthProvider::callTimestampNonceHandler'
  - oauthprovider.checkoauthrequest.md: 'OAuthProvider::checkOAuthRequest »'
  - index.md: PHP Manual
  - class.oauthprovider.md: OAuthProvider
title: 'OAuthProvider::calltokenHandler'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuthProvider::calltokenHandler

(PECL OAuth >= 1.0.0)

OAuthProvider::calltokenHandler — Викликати callback-функцію tokenNonceHandler

### Опис

```methodsynopsis
public OAuthProvider::calltokenHandler(): void
```

Викликати зареєстровану callback-функцію обробника токена, яка була задана за допомогою [OAuthProvider::tokenHandler()](oauthprovider.tokenhandler.md)

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Якщо callback-функція може бути викликана чи відсутня, то генерується помилка рівня **`E_ERROR`**

### Дивіться також

-   [OAuthProvider::tokenHandler()](oauthprovider.tokenhandler.md) \- Встановити обробник tokenHandler
