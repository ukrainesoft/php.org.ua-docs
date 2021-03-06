- [«crc32](function.crc32.md)
- [echo »](function.echo.md)

- [PHP Manual](index.md)
- [Функції для роботи з рядками](ref.strings.md)
- Необоротне хешування рядка

# crypt

(PHP 4, PHP 5, PHP 7, PHP 8)

crypt — Незворотне хешування рядка

**Увага**

Ця функція (поки що) небезпечна для обробки даних у двійковій формі!

### Опис

**crypt**(string `$string`, string `$salt`): string

**crypt()** повертає хешований рядок, отриманий за допомогою
стандартного алгоритму UNIX, що базується на DES або іншого алгоритму.
Функція [password_verify()](function.password-verify.md) сумісна з
**crypt()**. Отже, хеші паролів, створені **crypt()**, можуть
використовуватися в [password_verify()](function.password-verify.md).

Параметр `salt` є необов'язковим. Однак без `salt` функція
**crypt()** створює слабкий хеш. Якщо не використовувати `salt`, видається
помилка **`E_NOTICE`**. Переконайтеся, що ви використовуєте досить складну
сіль для кращої безпеки.

Функція [password_hash()](function.password-hash.md) використовує
складний хеш, генерує складну сіль і застосовує правильну кількість
раундів хешування автоматично.
[password_hash()](function.password-hash.md) є простою обгорткою
над **crypt()** та сумісна з існуючими хешами паролів. Тому
вітається використання
[password_hash()](function.password-hash.md).

Вид хешування визначається переданим аргументом salt (сіль). Якщо
сіль не вказана, буде автоматично згенерована стандартна випадкова
двосимвольна (DES) або дванадцятисимвольна (MD5) сіль, залежно
від доступності алгоритму MD5 crypt(). Обумовлена константа
**`CRYPT_SALT_LENGTH`** дозволяє визначити максимально доступну довжину
солі відповідно до алгоритмів.

Стандартна функція **crypt()** на основі DES повертає сіль як
перших двох символів рядка, що повертається. Крім того, вона використовує
тільки перші вісім символів рядка `string`, тому довші
рядки, що починаються з тих самих восьми символів, згенерують один і той же
результат (при використанні однакової солі).

Підтримуються такі типи хешей:

- **`CRYPT_STD_DES`** - Стандартне DES-шифрування з двосимвольною
сіллю з алфавіту "./0-9A-Za-z"./0-9A-Za-z". Використання інших
символів у солі спричинить відмови роботи crypt().
- **`CRYPT_EXT_DES`** - Розширене DES-шифрування. "Сіль" є
9-символьним рядком, що складається із символу підкреслення, за яким
слідують 4 символи лічильника ітерації та 4 символи солі. Кожна з цих
4-символьних рядків кодує 24 біти, найменший символ першим.
Значення від `0` до `63` кодуються як `./0-9A-Za-z`. Використання
неприпустимих символів у солі призведе до помилки crypt().
- **`CRYPT_MD5`** - MD5-шифрування з 12-символьною сіллю,
що починається з $1$
- **`CRYPT_BLOWFISH`** - Blowfish-шифрування з наступною сіллю:
"$2a$", "$2x$" або "$2y$", ваговий параметр з двох цифр, "$" та 22
цифри з алфавіту "./0-9A-Za-z". Використання інших символів у
солі спричинить повернення порожнього рядка. Ваговий параметр з
двох цифр є двійковим логарифмом лічильника ітерацій
нижче хешируючого алгоритму, заснованого на Blowfish, та
повинен бути в діапазоні 04-31, значення поза цим діапазоном
викликають відмову crypt(). Хеші "$2x$" потенційно слабкі; Хеші "$2a$"
сумісні та пом'якшують цю слабкість. Для нових хешей слід
використовувати "$2y$". Для повного розуміння ознайомтеся з [» цим розділом](https://www.php.net/security/crypt_blowfish.php).
- **`CRYPT_SHA256`** - хеш SHA-256 з шістнадцятисимвольною сіллю,
що починається з $5$. Якщо рядок із сіллю починається з
'rounds=\<N\>$', число N буде використано для позначення
кількості раундів хешування, за аналогією з ваговим параметром
Blowfish. За замовчуванням кількість раундів дорівнює 5000,
мінімально доступно 1000 та максимально 999,999,999. Будь-яке значення
поза цим діапазоном буде усічено до найближчого ліміту.
- **`CRYPT_SHA512`** - хеш SHA-512 з шістнадцятисимвольною сіллю,
що починається з $6$. Якщо рядок із сіллю починається з
'rounds=\<N\>$', число N буде використано для позначення
кількості раундів хешування, за аналогією з ваговим параметром
Blowfish. За замовчуванням кількість раундів дорівнює 5000,
мінімально доступно 1000 та максимально 999,999,999. Будь-яке значення
поза цим діапазоном буде усічено до найближчого ліміту.

### Список параметрів

`string`
Хешований рядок.

**Застереження**
При використанні алгоритму **`CRYPT_BLOWFISH`**, параметр `string`
обрізається до 72 байт.

`salt`
Необов'язковий параметр із сіллю, на якій буде засновано хешування.
Якщо не вказано, поведінка визначається за наявністю реалізованих
алгоритмів у системі може призвести до несподіваних результатів.

### Значення, що повертаються

Повертає хешований рядок або рядок коротший за 13 символів,
що гарантовано відрізняється від солі у разі виникнення помилки.

**Увага**

При валідації паролів повинні використовуватись функції порівняння рядків,
стійкі до атаки за часом, порівняння висновку функції **crypt()**
із відомим хешом. У PHP для цього є функція
[hash_equals()](function.hash-equals.md).

### Список змін

| Версія | Опис                             |
|--------|----------------------------------|
| 8.0.0  | salt більше не є необов'язковим. |

### Приклади

**Приклад #1 Приклад використання **crypt()****

`<?php// сіль буде згенерована автоматично; не рекомендуется$hashed_password = crypt('mypassword');/* Для проверки пароля в качестве параметра salt следует передавать результат работы   crypt() целиком во избежание проблем при использовании различных   алгоритмов (как уже было отмечено выше, стандартный DES-алгоритм   использует 2- символьну сіль, а MD5 - 12-символьну. */if (hash_equals($hashed_password, crypt($user_input, $hashed_password))) {  echo "Пароль вірний!";

**Приклад #2 Використання **crypt()** та htpasswd**

` <?php// пароль$password = 'mypassword';// отримання хешу, сіль генерується автоматично; не рекомендується$hash = crypt($password);?> `

**Приклад #3 Використання **crypt()** з різними видами хешей**

`<?php/* Наведена сіль є тільки прикладом. Не використовуйте цю ж сіль у вашому коді. Ви маємо згенерувати унікальну і правильну сіль для кожного пароля.
";echo 'Розширений DES: ',    crypt('rasmuslerdorf', '_J9..rasm'),    "
";echo 'MD5:          '',    crypt('rasmuslerdorf', '$1$rasmusle$'),    "
";echo 'Blowfish:     ',    crypt('rasmuslerdorf', '$2a$07$usesomesillystringforsalt$'),    "
";echo 'SHA-256:       ',    crypt('rasmuslerdorf', '$5$rounds=5000$usesomesillystringforsalt$'),    "
";echo 'SHA-512:       ',    crypt('rasmuslerdorf', '$6$rounds=5000$usesomesillystringforsalt$'),    "
";?> `

Результатом виконання цього прикладу буде щось подібне:

Стандартний DES: rl.3StKT.4T8M
Розширений DES: _J9..rasmBYk8r9AiWNc
MD5: $1$rasmusle$rISCgZzpwk3UhDidwXvin0
Blowfish: $2y$07$usesomesillystringfore2uDLvp1Ii2e./U9C8sBjqp8I90dH6hi
SHA-256: $5$rounds=5000$usesomesillystri$KqJWpanXZHKq2BOB43TSaYhEWsQ1Lr5QNyPCDH/Tp.6
SHA-512: $6$rounds=5000$usesomesillystri$D4IrlXatmP7rx3P3InaxBeoomnAihCKRVQP22JZ6EY47Wc6BkroIuUUBOov1i.S5KPgErtP/EN5mcO.ChWQ

### Примітки

> **Примітка**: Функція розшифровки відсутня, тому що **crypt()**
> використовує необоротний алгоритм хешування.

### Дивіться також

- [hash_equals()](function.hash-equals.md) - Порівняння рядків,
нечутливе до атак за часом
- [password_hash()](function.password-hash.md) - Створює хеш пароля
- [md5()](function.md5.md) - Повертає MD5-хеш рядки
- Сторінка керівництва Unix за вашою функцією crypt
