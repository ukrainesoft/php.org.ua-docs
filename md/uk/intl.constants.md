---
navigation:
  - intl.resources.md: « Типи ресурсів
  - intl.examples.md: Приклади »
  - index.md: PHP Manual
  - book.intl.md: intl
title: Обумовлені константи
---
# Обумовлені константи

**`INTL_ICU_VERSION`** (string)

Поточна версія бібліотеки ICU у вигляді чисел із точковими роздільниками.

**`INTL_MAX_LOCALE_LEN`** (int)

Визначає довжину імені локалі. Для PHP встановлено 80. Імена локалів більше цього значення не приймаються.

**`IDNA_DEFAULT`** (int)

Заборонити передачу невизначених кодів символів функції IDN і не перевіряти введення на відповідність правилам доменних імен ASCII.

**`IDNA_ALLOW_UNASSIGNED`** (int)

Дозволити передачу невизначених кодів символів функції IDN

**`IDNA_USE_STD3_RULES`** (int)

Перевірити введення функцій IDN на відповідність правилам доменних імен ASCII.

**`IDNA_CHECK_BIDI`** (int)

Перевірити, чи введення правил BiDi. Ігнорується у реалізації IDNA2003, яка завжди здійснює цю перевірку.

**`IDNA_CHECK_CONTEXTJ`** (int)

Перевірити, чи відповідає введення правилам CONTEXTJ. Ігнорується у реалізації IDNA2003, оскільки ця перевірка введена до IDNA2008.

**`IDNA_NONTRANSITIONAL_TO_ASCII`** (int)

Опція для ненаскрізної обробки [idnтоascii()](function.idn-to-ascii.html). Наскрізна обробка активована за умовчанням. Ігнорується у реалізації IDNA2003.

**`IDNA_NONTRANSITIONAL_TO_UNICODE`** (int)

Опція для ненаскрізної обробки [idnтоutf8()](function.idn-to-utf8.html). Наскрізна обробка активована за умовчанням. Ігнорується у реалізації IDNA2003.

**`INTL_IDNA_VARIANT_2003`** (int)

Використовувати алгоритм IDNA 2003 [idnтоutf8()](function.idn-to-utf8.html) і [idnтоascii()](function.idn-to-ascii.html). Встановлено за замовчуванням. Ця константа і те, що вона використовується за умовчанням, оголошено застарілим у PHP 7.2.0.

**`INTL_IDNA_VARIANT_UTS46`** (int)

Використовувати алгоритм UTS #46 [idnтоutf8()](function.idn-to-utf8.html) і [idnтоascii()](function.idn-to-ascii.html). Доступно з ICU 4.6.

**`IDNA_ERROR_EMPTY_LABEL`** (int)

**`IDNA_ERROR_LABEL_TOO_LONG`** (int)

**`IDNA_ERROR_DOMAIN_NAME_TOO_LONG`** (int)

**`IDNA_ERROR_LEADING_HYPHEN`** (int)

**`IDNA_ERROR_TRAILING_HYPHEN`** (int)

**`IDNA_ERROR_HYPHEN_3_4`** (int)

**`IDNA_ERROR_LEADING_COMBINING_MARK`** (int)

**`IDNA_ERROR_DISALLOWED`** (int)

**`IDNA_ERROR_PUNYCODE`** (int)

**`IDNA_ERROR_LABEL_HAS_DOT`** (int)

**`IDNA_ERROR_INVALID_ACE_LABEL`** (int)

**`IDNA_ERROR_BIDI`** (int)

**`IDNA_ERROR_CONTEXTJ`** (int)

При використанні алгоритму UTS #46 [idnтоutf8()](function.idn-to-utf8.html) і [idnтоascii()](function.idn-to-ascii.html)помилки повертаються у вигляді побітової маски
