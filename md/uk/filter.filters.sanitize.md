---
navigation:
  - filter.filters.validate.md: « Фільтри валідації даних
  - filter.filters.misc.md: Інші фільтри »
  - index.md: PHP Manual
  - filter.filters.md: Типи фільтрів
title: Очищаючі фільтри
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Очищаючі фільтри

**Список фільтрів, що очищають**

| Идентификатор | Имя | Флаги | Опис |
| --- | --- | --- | --- |
| **`FILTER_SANITIZE_EMAIL`** | "email" |  | Видаляє символи, окрім букв, цифр та символів \`\`!#$%&'\*+-=?^\_\`{ |
| **`FILTER_SANITIZE_ENCODED`** | "encoded" | **`FILTER_FLAG_STRIP_LOW`** **`FILTER_FLAG_STRIP_HIGH`** **`FILTER_FLAG_STRIP_BACKTICK`** **`FILTER_FLAG_ENCODE_LOW`** **`FILTER_FLAG_ENCODE_HIGH`** | Кодує рядок у формат URL і, якщо потрібно, видаляє або кодує спеціальні символи. |
| **`FILTER_SANITIZE_MAGIC_QUOTES`** | "magic\_quotes" |  | Застосовує функцію [addslashes()](function.addslashes.md). *ЗАСТАРІЛА* з PHP 7.3.0 та *ВИДАЛЕНО* з PHP 8.0.0, замість неї вказують **`FILTER_SANITIZE_ADD_SLASHES`** |
| **`FILTER_SANITIZE_ADD_SLASHES`** | "add\_slashes" |  | Застосовує функцію [addslashes()](function.addslashes.md). . (Доступно з PHP 7.3.0.) |
| **`FILTER_SANITIZE_NUMBER_FLOAT`** | "number\_float" | **`FILTER_FLAG_ALLOW_FRACTION`** **`FILTER_FLAG_ALLOW_THOUSAND`** **`FILTER_FLAG_ALLOW_SCIENTIFIC`** | Видаляє символи, крім цифр, `+-` і якщо потрібно, то і `.,eE` |
| **`FILTER_SANITIZE_NUMBER_INT`** | "number\_int" |  | Видаляє символи, окрім цифр та знаків плюса та мінуса. |
| **`FILTER_SANITIZE_SPECIAL_CHARS`** | "special\_chars" | **`FILTER_FLAG_STRIP_LOW`** **`FILTER_FLAG_STRIP_HIGH`** **`FILTER_FLAG_STRIP_BACKTICK`** **`FILTER_FLAG_ENCODE_HIGH`** | Кодує символи `'"<>&` та символи з ASCII-кодом менше 32 у HTML-сутності, і, якщо потрібно, видаляє або кодує інші спеціальні символи. |
| **`FILTER_SANITIZE_FULL_SPECIAL_CHARS`** | "full\_special\_chars" | **`FILTER_FLAG_NO_ENCODE_QUOTES`** | Еквівалент виклику функції [htmlspecialchars()](function.mdspecialchars.md)с параметром\*\*`ENT_QUOTES`\*\*. . Кодування лапок відключають установкою прапора **`FILTER_FLAG_NO_ENCODE_QUOTES`**. . Як і функція [htmlspecialchars()](function.mdspecialchars.md), цей фільтр враховує директиву [default\_charset](ini.core.md#ini.default-charset), і якщо в послідовності байтів буде виявлено неприпустимий для поточного кодування символ, весь рядок буде забракована, а результатом буде рядок нульової довжини. При встановленні цього фільтра як фільтр за замовчуванням враховують попередження, яке викладено нижче, воно розповідає про встановлення прапорів за умовчанням значення 0. |
| **`FILTER_SANITIZE_STRING`** | "string" | **`FILTER_FLAG_NO_ENCODE_QUOTES`** **`FILTER_FLAG_STRIP_LOW`** **`FILTER_FLAG_STRIP_HIGH`** **`FILTER_FLAG_STRIP_BACKTICK`** **`FILTER_FLAG_ENCODE_LOW`** **`FILTER_FLAG_ENCODE_HIGH`** **`FILTER_FLAG_ENCODE_AMP`** | Видаляє теги та кодує подвійні та одинарні лапки, а якщо потрібно, видаляє або кодує спеціальні символи. Кодування лапок можна вимкнути, встановивши **`FILTER_FLAG_NO_ENCODE_QUOTES`**. . (Оголошено *застарілим* починаючи з PHP 8.1.0, використовуйте замість нього функцію [htmlspecialchars()](function.mdspecialchars.md) |
| **`FILTER_SANITIZE_STRIPPED`** | "stripped" |  | Псевдонім фільтра "string". (Оголошено *застарілим* починаючи з PHP 8.1.0, використовуйте замість нього функцію [htmlspecialchars()](function.mdspecialchars.md) |
| **`FILTER_SANITIZE_URL`** | "url" |  | Видаляє символи, окрім букв, цифр і \`\`$-\_.+!\*'(),{} |
| **`FILTER_UNSAFE_RAW`** | "unsafe\_raw" | **`FILTER_FLAG_STRIP_LOW`** **`FILTER_FLAG_STRIP_HIGH`** **`FILTER_FLAG_STRIP_BACKTICK`** **`FILTER_FLAG_ENCODE_LOW`** **`FILTER_FLAG_ENCODE_HIGH`** **`FILTER_FLAG_ENCODE_AMP`** | Не діє, і, якщо потрібно, видаляє або кодує спеціальні символи. Цей фільтр - псевдонім фільтра **`FILTER_DEFAULT`** |

**Увага**

Якщо або в ini-файлі, або в конфігурації веб-сервера один із цих фільтрів вказаний як фільтр за замовчуванням, прапором за замовчуванням для нього буде значення \*\*`FILTER_FLAG_NO_ENCODE_QUOTES`\*\*Необходимо явно установить параметру filter.default\_flags значення 0, щоб за замовчуванням лапки кодувалися. Ось так:

**Приклад #1 Налаштування стандартного фільтра для роботи аналогічно функції htmlspecialchars**

```php
filter.default = full_special_chars
filter.default_flags = 0
```

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Фільтри **`FILTER_SANITIZE_STRING`**и**`FILTER_SANITIZE_STRIPPED`** оголошено застарілими. |
| 8.0.0 | Вилучено фільтр **`FILTER_SANITIZE_MAGIC_QUOTES`** |
| 7.3.0 | Як заміна **`FILTER_SANITIZE_MAGIC_QUOTES`** додано фільтр **`FILTER_SANITIZE_ADD_SLASHES`** |
| 7.3.0 | Фильтр\*\*`FILTER_SANITIZE_MAGIC_QUOTES`\*\* оголошено застарілим. |
