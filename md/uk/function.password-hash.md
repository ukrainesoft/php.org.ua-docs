- [«password_get_info](function.password-get-info.md)
- [password_needs_rehash »](function.password-needs-rehash.md)

- [PHP Manual](index.md)
- [Функції хешування паролів](ref.password.md)
- Створює хеш пароля

#password_hash

(PHP 5 \>= 5.5.0, PHP 7, PHP 8)

password_hash - Створює хеш пароля

### Опис

**password_hash**(string `$password`, string\|int\|null `$algo`, array
`$options` = []): string

**password_hash()** створює хеш пароля використовуючи сильний, необоротний
алгоритм хешування.

На даний момент підтримуються такі алгоритми:

- **`PASSWORD_DEFAULT`** - використовується алгоритм bcrypt (за замовчуванням
з PHP 5.5.0). Зверніть увагу, що алгоритм, що використовується
часом змінюватися на сильніший, коли такий додається до PHP.
Відповідно, і довжина результату може з часом змінюватися. В
рекомендується вибирати довжину поля для зберігання в базі
даних більше 60 символів (255 символів могло бути добрим
варіантом).
- **`PASSWORD_BCRYPT`** - використовує алгоритм **`CRYPT_BLOWFISH`**.
Генерує стандартний хеш, сумісний із генерованою функцією
[crypt()](function.crypt.md) за допомогою ідентифікатора
"$2y$". В результаті буде згенерований рядок завдовжки 60 символів
або **`false`** у разі виникнення помилки.
- **`PASSWORD_ARGON2I`** - Використовувати алгоритм хешування Argon2i.
Цей алгоритм доступний лише якщо PHP зібраний за допомогою Argon2.
- **`PASSWORD_ARGON2ID`** - Використовувати алгоритм хешування
Argon2id. Цей алгоритм доступний лише якщо PHP зібрано з підтримкою
Argon2.

Опції, що підтримуються для **`PASSWORD_BCRYPT`**:

- `salt` (string) – для самостійного завдання солі для хешування.
Зверніть увагу, що це призведе до перевизначення та
запобігання автоматичному створенню солі.

Якщо не задано, то **password_hash()** генеруватиме випадкову
сіль для кожного пароля, що хешується. Це кращий режим
роботи.

**Увага**
Ця опція оголошена застарілою. Рекомендується використовувати
сіль, що автоматично генерується. Починаючи з PHP 8.0.0, явно задана
сіль ігнорується.

- `cost` (int) - ставить необхідну алгоритмічну складність. Приклад
використання цього значення можна переглянути на сторінці
присвяченої функції [crypt()](function.crypt.md).

Якщо не встановлено, то буде використано значення за замовчуванням `10`.
Це хороша базова вартість, але ви можете її збільшити
Залежно від можливостей свого обладнання.

Опції, що підтримуються для **`PASSWORD_ARGON2I`** та
**`PASSWORD_ARGON2ID`**:

- `memory_cost` (int) - Максимальний розмір пам'яті (у кілобайтах),
яку можна використовувати для обчислення хешу Argon2. За замовчуванням
**`PASSWORD_ARGON2_DEFAULT_MEMORY_COST`**.

- `time_cost` (int) - Максимально можливий час, який можна
витратити на обчислення хешу Argon2. За замовчуванням
**`PASSWORD_ARGON2_DEFAULT_TIME_COST`**.

- `threads` (int) - Кількість потоків, які можна використовувати для
обчислення хешу Argon2. За замовчуванням
**`PASSWORD_ARGON2_DEFAULT_THREADS`**.

**Увага**
Доступно тільки тоді, коли PHP використовує libargon2, але не при
реалізації libsodium.

### Список параметрів

`password`
Користувальницький пароль.

**Застереження**
Використання алгоритму **`PASSWORD_BCRYPT`** призведе до обрізання поля
`password` до максимальної довжини 72 байти.

`algo`
[Константа](password.constants.md), що позначає алгоритм, що використовується
хешування пароля.

`options`
Асоціативний масив із опціями. За документацією щодо підтримуваних
опціям для кожного алгоритму зверніться до розділу [Константи алгоритмів хешування паролів](password.constants.md).

Якщо не задано, то буде використано стандартну вартість і сіль буде
генеруватися автоматично.

### Значення, що повертаються

Повертає пароль хешування.

Використаний алгоритм, вартість та сіль буде повернено як частину
хеша. Таким чином, інформація, необхідна для перевірки хешу
нього включено. Це дозволить функції
[password_verify()](function.password-verify.md) перевіряти хеш без
необхідності окремого зберігання інформації про солі та алгоритм.

### Список змін

| Версія | Опис                                                                                                |
|--------|-----------------------------------------------------------------------------------------------------|
| 8.0.0  | **password_hash()** більше не повертає **false** у разі виникнення помилки.                         |
| 8.0.0  | Параметр algo тепер припускає значення null.                                                        |
| 7.4.0  | Параметр algo зараз очікує рядок (string), але все ще приймає число (int) для зворотної сумісності. |
| 7.4.0  | Модуль sodium забезпечує альтернативну реалізацію паролів Argon2.                                   |
| 7.3.0  | Додано підтримку алгоритму хешування паролів Argon2id за допомогою **PASSWORD_ARGON2ID**.           |
| 7.2.0  | Додано підтримку хешируючого алгоритму Argon2i за допомогою **PASSWORD_ARGON2I**.                   |

### Приклади

**Приклад #1 Приклад використання **password_hash()****

` <?php/** * Ми просто хочемо захешувати свій пароль використовуючи настройки за замовчуванням. *Значить буде використаний BCRYPT і результат буде 60 символів довжиною. * * Помните, что алгоритм по умолчанию может измениться в будущем, так что * имеет смысл заранее позаботиться о том, чтобы система хранения хешей * смогла хранить более 60 символов (255 в самый раз) */echo password_hash("rasmuslerdorf", PASSWORD_DEFAULT) ;?> `

Результатом виконання цього прикладу буде щось подібне:

$2y$10$.vGA1O9wmRjrwAVXD98HNOgsNpDczlqm3Jq7KnEd1rVAGv3Fykk1a

**Приклад #2 Приклад використання **password_hash()** з ручним завданням
вартості**

` <?php/** * Тут мы увеличиваем алгоритмическую стоимость BCRYPT до 12. * Но это никак не скажется на длине полученного результата, она останется 60 символов */$options = [    'cost' => 12,];echo password_hash( "rasmuslerdorf", PASSWORD_BCRYPT, $options);?> `

Результатом виконання цього прикладу буде щось подібне:

$2y$12$QjSH496pcT5CEbzjD/vtVeH03tfHKFy36d4J0Ltp3lRtee9HDxY3K

**Приклад #3 Приклад пошуку хорошого значення вартості для
**password_hash()****

`<?php/** * Даний код замірить швидкість виконання операції хешування для вашого сервера * з різними значеннями алгоритмічної складності для визначення максимального * не             Хороше базове значення * лежить в діапазоні 8-10, але якщо ваш сервер досить потужний, то можна задати і більше. Даний скрипт шукає максимальне значення, при якому* хешування укладеться в 50 мілісекунд. */$timeTarget==0.05; // 50 мілісекунд.$cost = 8;do {    $cost++; $start = microtime(true); password_hash("test", PASSWORD_BCRYPT, ["cost" => $cost]); $end = microtime(true);} while (($end - $start) < $timeTarget);echo "Оптимальна вартість: " . $cost;?> `

Результатом виконання цього прикладу буде щось подібне:

Оптимальна вартість: 10

**Приклад #4 Приклад використання **password_hash()** з Argon2i**

`<?phpecho 'Хеш Argon2i: ' . password_hash('rasmuslerdorf', PASSWORD_ARGON2I);?> `

Результатом виконання цього прикладу буде щось подібне:

Хеш Argon2i: $argon2i$v=19$m=1024,t=2,p=2$YzJBSzV4TUhkMzc3d3laeg$zqU/1IN0/AogfP4cmSJI1vc8lpXRW9/S0sYY2i2jHT0

### Примітки

**Застереження**

Рекомендується використовувати автоматичну генерацію солі.
Ця функція самостійно створить хорошу сіль, якщо ви не будете їй
заважати підсовуючи свою.

Як було зазначено вище, опція `salt` була оголошена застарілою в PHP 7.0
і викликатиме відповідне попередження. Підтримка ручного
завдання солі може бути видалена у новіших версіях.

> **Примітка**:
>
> Рекомендується протестувати цю функцію на вашому залізі для
> Визначення оптимального значення алгоритмічної складності.
> Переконайтеся, що з вибраною складністю функція виконується швидше за 100
> мілісекунд для інтерактивних систем. Скрипт показаний вище допоможе
> вам вибрати потрібне значення.

> **Примітка**: Оновлення підтримуваних алгоритмів для цієї функції
> (або зміна значення за замовчуванням) зобов'язані дотримуватися правил:
>
> - Будь-який новий алгоритм повинен бути присутнім у ядрі як мінімум 1
> повний реліз PHP для того, щоб його можна було встановити
> замовчуванням. Таким чином, якщо, наприклад, новий алгоритм був
> додано до 7.5.5, то задати за замовчуванням його можна буде тільки в
> 7.7 (7.6 буде цим повним релізом, протягом якого він
> повинен бути присутнім, від 7.6.0 до 7.7.0). Але якщо новий алгоритм
> додано до 7.6.0, то його також можна буде задати за замовчуванням
>7.7.0.
> - Алгоритм за замовчуванням може бути змінено лише у повному релізі
> (7.3.0, 8.0.0 і т.д.), але не в проміжних. Єдине
> виняток - якщо у поточному алгоритмі знайдено критична
> уразливість.

### Дивіться також

- [password_verify()](function.password-verify.md) - Перевіряє,
чи відповідає пароль хешу
- [crypt()](function.crypt.md) - Необоротне хешування рядка
- [» Користувацька реалізація](https://github.com/ircmaxell/password_compat)
- [sodium_crypto_pwhash_str()](function.sodium-crypto-pwhash-str.md) -
Отримати ASCII-кодований хеш
