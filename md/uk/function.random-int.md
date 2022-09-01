---
navigation:
  - function.random-bytes.html: « randombytes
  - book.hash.html: Hash »
  - index.html: PHP Manual
  - ref.csprng.html: Функции CSPRNG
title: randomint
---
# randomint

(PHP 7, PHP 8)

randomint — Генерує криптографічно безпечні псевдовипадкові цілі числа

### Опис

```methodsynopsis
random_int(int $min, int $max): int
```

Генерує криптографічно випадкові цілі числа, придатні для використання в криптографічних цілях, де випадковість результату критична, наприклад, перемішування колоди карт для гри в покер.

Джерело випадкових величин, що використовуються цією функцією:

-   У Windows завжди використовується [**CryptGenRandom()**](https://msdn.microsoft.com/en-us/library/windows/desktop/aa379942(v=vs.85).aspx) Починаючи з PHP 7.2.0, замість нього завжди використовуватиметься [» CNG-API](https://docs.microsoft.com/en-us/windows/desktop/SecCNG/cng-portal)
-   У Linux, якщо доступний, використовується системний виклик [» getrandom(2)](http://man7.org/linux/man-pages/man2/getrandom.2.html)
-   На інших платформах використовується /dev/urandom.
-   Якщо доступні джерела випадкових величин відсутні, викидається виняток [Exception](class.exception.html)

> **Зауваження**: Ця функція була додана в PHP 7.0, а для версій з 5.2 до 5.6 включно доступна [» користувацька реалізація](https://github.com/paragonie/random_compat)

### Список параметрів

`min`

Нижня межа діапазону, з якого буде вибрано випадкове число. Повинна бути більшою або рівною **`PHP_INT_MIN`**

`max`

Верхня межа діапазону, з якого буде вибрано випадкове число. Повинна бути меншою або рівною **`PHP_INT_MAX`**

### Значення, що повертаються

Генерує криптографічно безпечне випадкове ціле число в діапазоні від `min` до `max`, включно.

### Помилки

-   Якщо відповідних джерел випадкових величин відсутні, то викидається виняток [Exception](class.exception.html)
-   Якщо встановлено некоректний параметр, викидається виняток [TypeError](class.typeerror.html)
-   Якщо поставити `max` менше ніж `min`, то буде викинуто виняток класу [Error](class.error.html)

### Приклади

**Приклад #1 Приклад **randomint()****

```php
<?php
var_dump(random_int(100, 999));
var_dump(random_int(-1000, 0));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(248)
int(-898)
```

### Дивіться також

-   [randombytes()](function.random-bytes.html) - Генерує криптографічно безпечні псевдовипадкові байти
