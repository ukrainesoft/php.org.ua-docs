Встановити параметр

-   [« OAuthProvider::reportProblem](oauthprovider.reportproblem.md)
    
-   [OAuthProvider::setRequestTokenPath »](oauthprovider.setrequesttokenpath.md)
    
-   [PHP Manual](index.md)
    
-   [OAuthProvider](class.oauthprovider.md)
    
-   Встановити параметр
    

# OAuthProvider::setParam

(PECL OAuth >= 1.0.0)

OAuthProvider::setParam — Встановити параметр

### Опис

```methodsynopsis
final public OAuthProvider::setParam(string $param_key, mixed $param_val = ?): bool
```

Встановлює параметр.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`param_key`

Ключ параметра.

`param_val`

Необов'язкове значення параметра.

Для виключення параметра з процесу перевірки підпису встановіть його на значення **`null`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [OAuthProvider::addRequiredParameter()](oauthprovider.addrequiredparameter.md) - Додати необхідні параметри