---
navigation:
  - oauthprovider.callconsumerhandler.md: '« OAuthProvider::callconsumerHandler'
  - oauthprovider.calltokenhandler.md: 'OAuthProvider::calltokenHandler »'
  - index.md: PHP Manual
  - class.oauthprovider.md: OAuthProvider
title: 'OAuthProvider::callTimestampNonceHandler'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuthProvider::callTimestampNonceHandler

(PECL OAuth >= 1.0.0)

OAuthProvider::callTimestampNonceHandler — Викликати callback-функцію timestampNonceHandler

### Опис

```methodsynopsis
public OAuthProvider::callTimestampNonceHandler(): void
```

Викликати зареєстровану callback-функцію обробника мітки часу, яка була задана за допомогою [OAuthProvider::timestampNonceHandler()](oauthprovider.timestampnoncehandler.md)

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Якщо callback-функція може бути викликана чи відсутня, то генерується помилка рівня **`E_ERROR`**

### Дивіться також

-   [OAuthProvider::timestampNonceHandler()](oauthprovider.timestampnoncehandler.md) \- Встановити обробник timestampNonceHandler
