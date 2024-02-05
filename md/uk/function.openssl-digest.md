---
navigation:
  - function.openssl-dh-compute-key.md: « openssl\_dh\_compute\_key
  - function.openssl-encrypt.md: openssl\_encrypt »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_digest
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_digest

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

openssl\_digest - Обчислення дайджесту

### Опис

```methodsynopsis
openssl_digest(string $data, string $digest_algo, bool $binary = false): string|false
```

Обчислює значення дайджесту для даних із допомогою зазначеного методу. Повертає необроблений рядок чи рядок шістнадцяткових чисел.

### Список параметрів

`data`

Дані.

`digest_algo`

Метод обчислення дайджесту, наприклад "sha256". Список доступних методів можна отримати за допомогою [openssl\_get\_md\_methods()](function.openssl-get-md-methods.md)

`binary`

Якщо **`true`**, то буде повернено необроблений рядок. Інакше буде повернуто рядок шістнадцяткових чисел.

### Значення, що повертаються

Повертає обчислений дайджест або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо параметр `digest_algo` передано невідомий метод.

### Дивіться також

-   [openssl\_get\_md\_methods()](function.openssl-get-md-methods.md) \- Отримати список доступних методів хешування
