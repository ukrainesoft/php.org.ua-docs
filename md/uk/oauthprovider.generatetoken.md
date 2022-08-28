Генерація випадкового токена

-   [« OAuthProvider::consumerHandler](oauthprovider.consumerhandler.html)
    
-   [OAuthProvider::is2LeggedEndpoint »](oauthprovider.is2leggedendpoint.html)
    
-   [PHP Manual](index.html)
    
-   [OAuthProvider](class.oauthprovider.html)
    
-   Генерація випадкового токена
    

# OAuthProvider::generateToken

(PECL OAuth >= 1.0.0)

OAuthProvider::generateToken - Генерація випадкового токена

### Опис

```methodsynopsis
final public static OAuthProvider::generateToken(int $size, bool $strong = false): string
```

Генерує рядок псевдовипадкових байт.

### Список параметрів

`size`

Довжина токена в байтах.

`strong`

Встановлення в **`true`** призведе до використання `/dev/random`, в іншому випадку буде використаний неблокуючий `/dev/urandom`. У Windows цей параметр буде проігноровано.

### Значення, що повертаються

Згенерований токен у вигляді рядка байт.

### Помилки

Якщо параметр `strong` заданий як **`true`**, то буде видана помилка рівня **`E_WARNING`**, у випадку, якщо для заповнення випадкових байт, що залишилися (наприклад, якщо було знайдено недостатньо випадкових даних) буде використана стара реалізація [rand()](function.rand.html)

### Приклади

**Приклад #1 Приклад використання **OAuthProvider::generateToken()****

```php
<?php
$p = new OAuthProvider();

$t = $p->generateToken(4);

echo strlen($t),  PHP_EOL;
echo bin2hex($t), PHP_EOL;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
4
b6a82c27
```

### Примітки

> **Зауваження**
> 
> Якщо в системі недостатньо випадкових даних, то для генерації байт, що бракують, ця функція буде використовувати звичайну функцію [rand()](function.rand.html)

### Дивіться також

-   [openssl\_random\_pseudo\_bytes()](function.openssl-random-pseudo-bytes.html) - Генерує псевдовипадкову послідовність байт
-   [mcrypt\_create\_iv()](function.mcrypt-create-iv.html) - Створити ініціалізуючий вектор (Initialization Vector або IV) із випадкового джерела