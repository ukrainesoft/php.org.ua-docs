---
navigation:
  - oauthprovider.consumerhandler.md: '« OAuthProvider::consumerHandler'
  - oauthprovider.is2leggedendpoint.md: 'OAuthProvider::is2LeggedEndpoint »'
  - index.md: PHP Manual
  - class.oauthprovider.md: OAuthProvider
title: 'OAuthProvider::generateToken'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Установка в\*\*`true`\*\* призведе до використання `/dev/random`, в іншому випадку буде використаний неблокуючий `/dev/urandom`. У Windows цей параметр буде проігноровано.

### Значення, що повертаються

Згенерований токен у вигляді рядка байт.

### Помилки

Якщо параметр `strong`задан как\*\*`true`\*\*, то буде видана помилка рівня **`E_WARNING`**, у випадку, якщо для заповнення випадкових байт, що залишилися (наприклад, якщо було знайдено недостатньо випадкових даних) буде використана стара реалізація [rand()](function.rand.md)

### Приклади

**Пример #1 Пример использования**OAuthProvider::generateToken()\*\*\*\*

```php
<?php
$p = new OAuthProvider();

$t = $p->generateToken(4);

echo strlen($t),  PHP_EOL;
echo bin2hex($t), PHP_EOL;

?>
```

Висновок наведеного прикладу буде схожим на:

```
4
b6a82c27
```

### Примітки

> **Зауваження** :
> 
> Якщо в системі недостатньо випадкових даних, то для генерації байт, що бракують, ця функція буде використовувати звичайну функцію [rand()](function.rand.md)

### Дивіться також

-   [openssl\_random\_pseudo\_bytes()](function.openssl-random-pseudo-bytes.md) \- Генерує псевдовипадкову послідовність байт
-   [mcrypt\_create\_iv()](function.mcrypt-create-iv.md) \- Створити ініціалізуючий вектор (Initialization Vector або IV) із випадкового джерела
