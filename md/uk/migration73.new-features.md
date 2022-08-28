Нові можливості

-   [« Миграция с PHP 7.2.x на PHP 7.3.x](migration73.html)
    
-   [Новые функции »](migration73.new-functions.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 7.2.x на PHP 7.3.x](migration73.html)
    
-   Нові можливості
    

## Нові можливості

### Ядро PHP

#### Гнучкіший синтаксис Heredoc і Nowdoc

Після ідентифікатора, що закриває, в doc-рядках більше не потрібно ставити крапку з комою або новий рядок. Крім того, ідентифікатор, що закриває, може бути з відступом, і в цьому випадку він буде видалений з усіх рядків в doc-рядку.

#### Деструктурування масиву підтримує присвоєння за посиланнями

Деструктурування масиву тепер підтримує присвоєння посилань за допомогою синтаксису `[&$a, [$b, &$c]] = $d`. Те саме підтримується і для [list()](function.list.html)

#### Оператор встаніприймає літерали

Оператор `instanceof` тепер підтримує літерали як перший операнда, і в цьому випадку результат буде завжди **`false`**

#### Виняток CompileError замість деяких помилок компіляції

Додано новий виняток [CompileError](class.compileerror.html), що успадковується від [ParseError](class.parseerror.html). Невелика кількість помилок компіляції тепер викидатиме [CompileError](class.compileerror.html) замість створення фатальної помилки. В даний час це впливає лише на помилки компіляції, які можуть бути створені [token\_get\_all()](function.token-get-all.html) в режимі **`TOKEN_PARSE`**, але в майбутньому може бути перетворено більше помилок.

#### У викликах дозволена завершальна кома

Завершальні коми у викликах функцій та методів тепер дозволені.

#### Підтримка Argon2id

З аргументом **\-with-password-argon2=dir** скрипта configure тепер підтримуються обидва хеші, як Argon2i, так і Argon2id, у функціях [password\_hash()](function.password-hash.html) [password\_verify()](function.password-verify.html) [password\_get\_info()](function.password-get-info.html) і [password\_needs\_rehash()](function.password-needs-rehash.html). Паролі можуть бути хешовані та перевірені, використовуючи константу **`PASSWORD_ARGON2ID`**. Підтримка обох алгоритмів Argon2i та Argon2id у функціях сімейства **password** тепер вимагає, щоб PHP був скомпільований із бібліотекою libargon2 версії ≥ 20161029.

### Менеджер процесів FastCGI

Для налаштування логування FPM були додані нові опції:

`log_limit`

Ця глобальна опція може використовуватися для встановлення ліміту логування для рядка логування, що дозволяє записувати повідомлення довжиною понад 1024 символи без перенесення. Також виправляє різні проблеми із упаковкою (wrapping).

`log_buffering`

Ця глобальна опція дозволяє вести експериментальне логування без додаткової буферизації.

`decorate_workers_output`

Цей варіант пула дозволяє відключити відмітку виводу (output decoration) для обробників, коли `catch_workers_output` включено.

### Функції BC Math

Функція [bcscale()](function.bcscale.html) тепер також може використовуватися як геттер для вилучення поточного масштабу.

### Полегшений протокол доступу до каталогів (LDAP)

Було додано повну підтримку LDAP Controls до функцій запитів [LDAP](book.ldap.html) і [ldap\_parse\_result()](function.ldap-parse-result.html)

-   Доданий параметр `$serverctrls` для відправлення керування сервером у функціях [ldap\_add()](function.ldap-add.html) [ldap\_mod\_replace()](function.ldap-mod-replace.html) [ldap\_mod\_add()](function.ldap-mod-add.html) [ldap\_mod\_del()](function.ldap-mod-del.html) [ldap\_rename()](function.ldap-rename.html) [ldap\_compare()](function.ldap-compare.html) [ldap\_delete()](function.ldap-delete.html) [ldap\_modify\_batch()](function.ldap-modify-batch.html) [ldap\_search()](function.ldap-search.html) [ldap\_list()](function.ldap-list.html) і [ldap\_read()](function.ldap-read.html)
-   Доданий параметр `$serverctrls` для отримання керування з сервера до функцій [ldap\_parse\_result()](function.ldap-parse-result.html)
-   Підтримка **`LDAP_OPT_SERVER_CONTROLS`** і **`LDAP_OPT_CLIENT_CONTROLS`** у функціях [ldap\_get\_option()](function.ldap-get-option.html) і [ldap\_set\_option()](function.ldap-set-option.html) було виправлено.

### Функції мультибайтових рядків

#### Повна підтримка case-mapping та case-folding

Додано підтримку повного процесу перетворення регістру символів (case-mapping) та порівняння на ідентичність різних регістрів (case-folding). На відміну від простого case-mapping, повне case-mapping може змінити довжину рядка. Приклад:

```php
<?php
mb_strtoupper("Straße");
// Выведет STRAßE в PHP 7.2
// Выведет STRASSE в PHP 7.3
?>
```

Різні режими перетворення та порівняння регістру символів доступні у функції [mb\_convert\_case()](function.mb-convert-case.html)

-   **`MB_CASE_LOWER`** (використовується [mb\_strtolower()](function.mb-strtolower.html)
-   **`MB_CASE_UPPER`** (використовується [mb\_strtoupper()](function.mb-strtoupper.html)
-   **`MB_CASE_TITLE`**
-   **`MB_CASE_FOLD`**
-   **`MB_CASE_LOWER_SIMPLE`**
-   **`MB_CASE_UPPER_SIMPLE`**
-   **`MB_CASE_TITLE_SIMPLE`**
-   **`MB_CASE_FOLD_SIMPLE`** (використовується нечутливими до регістру операціями)

Виконує лише безумовний, незалежний від мови, повний процес перетворення.

#### Операції, нечутливі до регістру, використовують case-folding

Рядкові операції без урахування регістру тепер використовують case-folding замість case-mapping регістру при порівнянні. Це означає, що тепер більше символів вважатимуться (без урахування регістру) рівними.

#### МБCASETITLE виконує перетворення title-case

Функція [mb\_convert\_case()](function.mb-convert-case.html) з **`MB_CASE_TITLE`** тепер виконує перетворення title-case в залежності від властивостей Unicode, заснованих на Cased та CaseIgnorable. Зокрема, це також покращує обробку лапок та апострофів.

#### Підтримка Unicode 11

Таблиці даних [мультибайтовых строк](book.mbstring.html) були оновлені до Юнікод версії 11.

#### Підтримка великих рядків

[Функции мультибайтовых строк](ref.mbstring.html) тепер коректно підтримують рядки розміром понад 2 Гб.

#### Поліпшення продуктивності

Продуктивність модуля [мультибайтовых строк](book.mbstring.html) була значно повсюдно покращена. Найбільші покращення у функціях перетворення регістру.

#### Підтримка іменованих фрагментів

Функції `mb_ereg_*` Тепер підтримують іменовані фрагменти. Відповідні функції, такі як [mb\_ereg()](function.mb-ereg.html), тепер повертатимуть іменовані фрагменти як зі своїм номером групи, і зі своїм ім'ям, аналогічно PCRE:

```php
<?php
mb_ereg('(?<word>\w+)', '国', $matches);
// => [0 => "国", 1 => "国", "word" => "国"];
?>
```

Крім того, функція [mb\_ereg\_replace()](function.mb-ereg-replace.html) тепер підтримує позначення `\k<>` і `\k''` для посилання на іменовані фрагменти в рядку, що замінює:

```php
<?php
mb_ereg_replace('\s*(?<word>\w+)\s*', "_\k<word>_\k'word'_", ' foo ');
// => "_foo_foo_"
?>
```

`\k<>` і `\k''` також можуть використовуватися для нумерованих посилань, які також працюють із номерами груп більше 9.

### Readline

У функції [readline\_info()](function.readline-info.html) додано підтримку параметрів `completion_append_character` і `completion_suppress_append`. Ці опції доступні, тільки якщо PHP скомпільовано з бібліотекою libreadline (а не libedit).