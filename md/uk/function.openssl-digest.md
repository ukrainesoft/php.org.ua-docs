Обчислення дайджесту

-   [« opensslдхcomputekey](function.openssl-dh-compute-key.html)
    
-   [opensslencrypt »](function.openssl-encrypt.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Обчислення дайджесту
    

# openssldigest

(PHP 5> = 5.3.0, PHP 7, PHP 8)

openssldigest - Обчислення дайджесту

### Опис

```methodsynopsis
openssl_digest(string $data, string $digest_algo, bool $binary = false): string|false
```

Обчислює значення дайджесту для даних із допомогою зазначеного методу. Повертає необроблений рядок чи рядок шістнадцяткових чисел.

### Список параметрів

`data`

Дані.

`digest_algo`

Метод обчислення дайджесту, наприклад "sha256". Список доступних методів можна отримати за допомогою [opensslgetмдmethods()](function.openssl-get-md-methods.html)

`binary`

Якщо **`true`**, то буде повернено необроблений рядок. Інакше буде повернуто рядок шістнадцяткових чисел.

### Значення, що повертаються

Повертає обчислений дайджест або **`false`** у разі виникнення помилки.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо параметр `digest_algo` передано невідомий метод.

### Дивіться також

-   [opensslgetмдmethods()](function.openssl-get-md-methods.html) - Отримати список доступних методів хешування