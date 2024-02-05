---
navigation:
  - oauthprovider.addrequiredparameter.md: '« OAuthProvider::addRequiredParameter'
  - oauthprovider.calltimestampnoncehandler.md: 'OAuthProvider::callTimestampNonceHandler »'
  - index.md: PHP Manual
  - class.oauthprovider.md: OAuthProvider
title: 'OAuthProvider::callconsumerHandler'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuthProvider::callconsumerHandler

(No version information available, might only be in Git)

OAuthProvider::callconsumerHandler — Викликати callback-функцію consumerNonceHandler

### Опис

```methodsynopsis
public OAuthProvider::callconsumerHandler(): void
```

Викликати зареєстровану callback-функцію, яка була задана за допомогою [OAuthProvider::consumerHandler()](oauthprovider.consumerhandler.md)

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Якщо callback-функція може бути викликана чи відсутня, то генерується помилка рівня **`E_ERROR`**

### Дивіться також

-   [OAuthProvider::consumerHandler()](oauthprovider.consumerhandler.md) \- Встановити обробник consumerHandler
