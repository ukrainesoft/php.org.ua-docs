Генерує криптографічно безпечні псевдовипадкові байти

-   [« Функции CSPRNG](ref.csprng.html)
    
-   [random\_int »](function.random-int.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CSPRNG](ref.csprng.html)
    
-   Генерує криптографічно безпечні псевдовипадкові байти
    

# randombytes

(PHP 7, PHP 8)

randombytes - Генерує криптографічно безпечні псевдовипадкові байти

### Опис

```methodsynopsis
random_bytes(int $length): string
```

Генерує рядок криптографічно випадкових байт довільної довжини, яку можна використовувати з криптографічною метою, наприклад, для генерації солі, ключів або векторів ініціалізації.

Джерело випадкових величин, що використовуються цією функцією:

-   У Windows завжди використовується [» **CryptGenRandom()**](https://msdn.microsoft.com/en-us/library/windows/desktop/aa379942(v=vs.85).aspx) Починаючи з PHP 7.2.0, замість нього завжди використовуватиметься [» CNG-API](https://docs.microsoft.com/en-us/windows/desktop/SecCNG/cng-portal)
-   У Linux, якщо доступний, використовується системний виклик [» getrandom(2)](http://man7.org/linux/man-pages/man2/getrandom.2.html)
-   На інших платформах використовується /dev/urandom.
-   Якщо доступні джерела випадкових величин відсутні, викидається виняток [Exception](class.exception.html)

> **Зауваження**: Ця функція була додана в PHP 7.0, а для версій з 5.2 до 5.6 включно доступна [» пользовательская реализация](https://github.com/paragonie/random_compat)

### Список параметрів

`length`

Довжина генерованого рядка в байтах.

### Значення, що повертаються

Повертає рядок, що складається із заданої кількості криптографічно безпечних байт.

### Помилки

-   Якщо відповідних джерел випадкових величин відсутні, то викидається виняток [Exception](class.exception.html)
-   Якщо встановлено некоректний параметр, викидається виняток [TypeError](class.typeerror.html)
-   Якщо буде задана некоректна довжина `length`, то буде викинуто виняток класу [Error](class.error.html)

### Приклади

**Приклад #1 Приклад використання **randombytes()****

```php
<?php
$bytes = random_bytes(5);
var_dump(bin2hex($bytes));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(10) "385e33f741"
```

### Дивіться також

-   [random\_int()](function.random-int.html) - Генерує криптографічно безпечні псевдовипадкові цілі числа
-   [openssl\_random\_pseudo\_bytes()](function.openssl-random-pseudo-bytes.html) - Генерує псевдовипадкову послідовність байт
-   [bin2hex()](function.bin2hex.html) - Перетворює бінарні дані на шістнадцяткове подання