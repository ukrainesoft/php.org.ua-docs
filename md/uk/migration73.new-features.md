---
navigation:
  - migration73.md: « Міграція з PHP 7.2.x на PHP 7.3.x
  - migration73.new-functions.md: Нові функції »
  - index.md: PHP Manual
  - migration73.md: Міграція з PHP 7.2.x на PHP 7.3.x
title: Нові можливості
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Нові можливості

### Ядро PHP

#### Гнучкіший синтаксис Heredoc і Nowdoc

Після ідентифікатора, що закриває, в doc-рядках більше не потрібно ставити крапку з комою або новий рядок. Крім того, ідентифікатор, що закриває, може бути з відступом, і в цьому випадку він буде видалений з усіх рядків в doc-рядку.

#### Деструктурування масиву підтримує присвоєння за посиланнями

Деструктурування масиву тепер підтримує присвоєння посилань за допомогою синтаксису `[&$a, [$b, &$c]] = $d`. Те саме підтримується і для [list()](function.list.md)

#### Оператор встануприймає літерали

Оператор`instanceof` тепер підтримує літерали як перший операнда, і в цьому випадку результат буде завжди **`false`**

#### Виняток CompileError замість деяких помилок компіляції

Добавлено новое исключение[CompileError](class.compileerror.md), що успадковується від [ParseError](class.parseerror.md). Невелика кількість помилок компіляції тепер викидатиме [CompileError](class.compileerror.md) замість створення фатальної помилки. В даний час це впливає лише на помилки компіляції, які можуть бути створені [token\_get\_all()](function.token-get-all.md)в режиме\*\*`TOKEN_PARSE`\*\*, але в майбутньому може бути перетворено більше помилок.

#### У викликах дозволена завершальна кома

Завершальні коми у викликах функцій та методів тепер дозволені.

#### Підтримка Argon2id

З аргументом **\--with-password-argon2\[=dir\]** скрипта configure тепер підтримуються обидва хеші, як Argon2i, так і Argon2id, у функціях [password\_hash()](function.password-hash.md) [password\_verify()](function.password-verify.md) [password\_get\_info()](function.password-get-info.md) і [password\_needs\_rehash()](function.password-needs-rehash.md). Паролі можуть бути хешовані та перевірені, використовуючи константу **`PASSWORD_ARGON2ID`**. Підтримка обох алгоритмів Argon2i та Argon2id у функціях сімейства **password\_\*()** тепер вимагає, щоб PHP був скомпільований з бібліотекою libargon2 версії ≥20161029.

### Менеджер процесів FastCGI

Для налаштування логування FPM були додані нові опції:

`log_limit`

Ця глобальна опція може бути використана для встановлення ліміту логування для рядка логування, що дозволяє записувати повідомлення довжиною більше 1024 символів без перенесення. Також виправляє різні проблеми із упаковкою (wrapping).

`log_buffering`

Ця глобальна опція дозволяє вести експериментальне логування без додаткової буферизації.

`decorate_workers_output`

Цей варіант пула дозволяє відключити відмітку виводу (output decoration) для обробників, коли `catch_workers_output`включена.

### Функції BC Math

Функция[bcscale()](function.bcscale.md) тепер також може використовуватися як геттер для вилучення поточного масштабу.

### Полегшений протокол доступу до каталогів (LDAP)

Було додано повну підтримку LDAP Controls до функцій запитів [LDAP](book.ldap.md) і [ldap\_parse\_result()](function.ldap-parse-result.md) :

-   Добавлен параметр`$serverctrls`для відправлення керування сервером у функціях[ldap\_add()](function.ldap-add.md) [ldap\_mod\_replace()](function.ldap-mod-replace.md) [ldap\_mod\_add()](function.ldap-mod-add.md) [ldap\_mod\_del()](function.ldap-mod-del.md) [ldap\_rename()](function.ldap-rename.md) [ldap\_compare()](function.ldap-compare.md) [ldap\_delete()](function.ldap-delete.md) [ldap\_modify\_batch()](function.ldap-modify-batch.md) [ldap\_search()](function.ldap-search.md) [ldap\_list()](function.ldap-list.md) і [ldap\_read()](function.ldap-read.md)
-   Добавлен параметр`$serverctrls`для отримання керування з сервера до функцій[ldap\_parse\_result()](function.ldap-parse-result.md)
-   Поддержка\*\*`LDAP_OPT_SERVER_CONTROLS`** і **`LDAP_OPT_CLIENT_CONTROLS`\*\*у функціях[ldap\_get\_option()](function.ldap-get-option.md) і [ldap\_set\_option()](function.ldap-set-option.md)було виправлено.

### Функції мультибайтових рядків

#### Повна підтримка case-mapping та case-folding

Додано підтримку повного процесу перетворення регістру символів (case-mapping) та порівняння на ідентичність різних регістрів (case-folding). На відміну від простого case-mapping, повне case-mapping може змінити довжину рядка. Приклад:

```php
<?php
mb_strtoupper("Straße");
// Выведет STRAßE в PHP 7.2
// Выведет STRASSE в PHP 7.3
?>
```

Різні режими перетворення та порівняння регістру символів доступні у функції [mb\_convert\_case()](function.mb-convert-case.md) :

-   **`MB_CASE_LOWER`**(використовується[mb\_strtolower()](function.mb-strtolower.md)) .
-   **`MB_CASE_UPPER`**(використовується[mb\_strtoupper()](function.mb-strtoupper.md)) .
-   **`MB_CASE_TITLE`**
-   **`MB_CASE_FOLD`**
-   **`MB_CASE_LOWER_SIMPLE`**
-   **`MB_CASE_UPPER_SIMPLE`**
-   **`MB_CASE_TITLE_SIMPLE`**
-   **`MB_CASE_FOLD_SIMPLE`**(використовується нечутливими до регістру операціями)

Виконує лише безумовний, незалежний від мови, повний процес перетворення.

#### Операції, нечутливі до регістру, використовують case-folding

Рядкові операції без урахування регістру тепер використовують case-folding замість case-mapping регістру при порівнянні. Це означає, що тепер більше символів вважатимуться (без урахування регістру) рівними.

#### MB\_CASE\_TITLE виконує перетворення title-case

Функция[mb\_convert\_case()](function.mb-convert-case.md)с\*\*`MB_CASE_TITLE`\*\* тепер виконує перетворення title-case в залежності від властивостей Unicode, заснованих на Cased та CaseIgnorable. Зокрема, це також покращує обробку лапок та апострофів.

#### Підтримка Unicode 11

Таблиці даних [мультибайтових рядків](book.mbstring.md) були оновлені до Юнікод версії 11.

#### Підтримка великих рядків

[Функції мультибайтових рядків](ref.mbstring.md) тепер коректно підтримують рядки розміром понад 2 Гб.

#### Поліпшення продуктивності

Продуктивність модуля [мультибайтових рядків](book.mbstring.md) була значно повсюдно покращена. Найбільші покращення у функціях перетворення регістру.

#### Підтримка іменованих фрагментів

Функції `mb_ereg_*` Тепер підтримують іменовані фрагменти. Відповідні функції, такі як [mb\_ereg()](function.mb-ereg.md), тепер повертатимуть іменовані фрагменти як з їх номером групи, так і з їх ім'ям, аналогічно PCRE:

```php
<?php
mb_ereg('(?<word>\w+)', '国', $matches);
// => [0 => "国", 1 => "国", "word" => "国"];
?>
```

Крім того, функція [mb\_ereg\_replace()](function.mb-ereg-replace.md) тепер підтримує позначення `\k<>`и`\k''` для посилання на іменовані фрагменти в рядку, що замінює:

```php
<?php
mb_ereg_replace('\s*(?<word>\w+)\s*', "_\k<word>_\k'word'_", ' foo ');
// => "_foo_foo_"
?>
```

`\k<>`и`\k''` також можуть використовуватися для нумерованих посилань, які також працюють із номерами груп більше 9.

### Readline

У функції [readline\_info()](function.readline-info.md)добавлена поддержка параметров`completion_append_character`и`completion_suppress_append`. Ці опції доступні, тільки якщо PHP скомпільовано з бібліотекою libreadline (а не libedit).
