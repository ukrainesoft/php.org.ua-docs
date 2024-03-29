---
navigation:
  - function.hash-copy.md: « hash\_copy
  - function.hash-file.md: hash\_file »
  - index.md: PHP Manual
  - ref.hash.md: Функції Hash
title: hash\_equals
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# hash\_equals

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

hash\_equals — Порівнює рядки без ризику атаки за часом

### Опис

```methodsynopsis
hash_equals(string $known_string, string $user_string): bool
```

Порівнює два рядки на ідентичність так, що значення параметра `known_string` не можна розкрити методами, що базуються на знанні часу виконання функції.

Цю функцію можна застосовувати для зниження ризику атак часу. Звичайне порівняння через оператор `===` буде займати різний час залежно від того, різні це значення чи ні і в якій позиції перша відмінність буде знайдена, так розкривається значення параметра `known_string`

**Застереження**

Увага! Передавати отриманий від користувача рядок необхідно на другий параметр, а не на перший.

### Список параметрів

`known_string`

Відомий рядок (string), який має триматися в секреті.

`user_string`

Користувальницький рядок (string) для порівняння.

### Значення, що повертаються

Повертає **`true`**, якщо рядки ідентичні, та **`false`**, якщо ні.

### Приклади

**Приклад #1 Приклад використання** hash\_equals()\*\*\*\*

```php
<?php
$secretKey = '8uRhAeH89naXfFXKGOEj';

// Значение и подпись получены от пользователя, наПриклад, содержались в URL-адресе
// и были извлечены из глобальной переменной $_GET.
$value = 'username=rasmuslerdorf';
$signature = '8c35009d3b50caf7f5d2c1e031842e6b7823a1bb781d33c5237cd27b57b5f327';

if (hash_equals(hash_hmac('sha256', $value, $secretKey), $signature)) {
    echo "Значение подписано правильно.", PHP_EOL;
} else {
    echo "Значение было подделано.", PHP_EOL;
}
?>
```

Результат виконання наведеного прикладу:

```
Значение подписано правильно.
```

### Примітки

> **Зауваження** :
> 
> Для успішного порівняння обидва аргументи мають бути однієї довжини. Якщо передано аргументи різної довжини, то буде негайно повернено **`false`** і довжина відомого рядка може бути визначена у разі атаки за часом.

### Дивіться також

-   [hash\_hmac()](function.hash-hmac.md) \- Генерація хеш-коду на основі ключа, використовуючи метод HMAC
