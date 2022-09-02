---
navigation:
  - filter.filters.validate.md: « Фільтри валідації даних
  - filter.filters.misc.md: Інші фільтри »
  - index.md: PHP Manual
  - filter.filters.md: Типи фільтрів
title: Очищаючі фільтри
---
## Очищаючі фільтри

**Список фільтрів, що очищають**

| Идентификатор | Имя | Флаги | Описание |
| --- | --- | --- | --- |
| **`FILTER_SANITIZE_EMAIL`** | "email" |  | Видаляє всі символи, окрім букв, цифр і \`\`!#$%&'\*+-=?^\_\`{ |
| **`FILTER_SANITIZE_ENCODED`** | "encoded" | **`FILTER_FLAG_STRIP_LOW`** **`FILTER_FLAG_STRIP_HIGH`** **`FILTER_FLAG_STRIP_BACKTICK`** **`FILTER_FLAG_ENCODE_LOW`** **`FILTER_FLAG_ENCODE_HIGH`** | Кодує рядок у формат URL, у разі потреби видаляє або кодує спеціальні символи. |
| **`FILTER_SANITIZE_MAGIC_QUOTES`** | "magicquotes" |  | Застосовується функція [addslashes()](function.addslashes.md). *ЗАСТАРІЛА* з PHP 7.3.0 та *ВИДАЛЕНО* з PHP 8.0.0, використовуйте замість неї **`FILTER_SANITIZE_ADD_SLASHES`** |
| **`FILTER_SANITIZE_ADD_SLASHES`** | "addslashes" |  | Застосовується функція [addslashes()](function.addslashes.md). (Доступно з PHP 7.3.0) |
| **`FILTER_SANITIZE_NUMBER_FLOAT`** | "numberfloat" | **`FILTER_FLAG_ALLOW_FRACTION`** **`FILTER_FLAG_ALLOW_THOUSAND`** **`FILTER_FLAG_ALLOW_SCIENTIFIC`** | Видаляє всі символи, крім цифр, `+-` і, за необхідності, `.,eE` |
| **`FILTER_SANITIZE_NUMBER_INT`** | "numberint" |  | Видаляє всі символи, крім цифр та знаків плюса та мінуса. |
| **`FILTER_SANITIZE_SPECIAL_CHARS`** | "specialchars" | **`FILTER_FLAG_STRIP_LOW`** **`FILTER_FLAG_STRIP_HIGH`** **`FILTER_FLAG_STRIP_BACKTICK`** **`FILTER_FLAG_ENCODE_HIGH`** | Екранує HTML-символи `'"<>&` та символи з ASCII-кодом, меншим 32, при необхідності видаляє або кодує інші спеціальні символи. |
| **`FILTER_SANITIZE_FULL_SPECIAL_CHARS`** | "fullspecialchars" | **`FILTER_FLAG_NO_ENCODE_QUOTES`** | Еквівалентно виклику [htmlspecialchars()](function.htmlspecialchars.md) із встановленим параметром **`ENT_QUOTES`**. Кодування лапок може бути вимкнено за допомогою установки прапора **`FILTER_FLAG_NO_ENCODE_QUOTES`**. Аналогічно [htmlspecialchars()](function.htmlspecialchars.md), цей фільтр бере до уваги [defaultcharset](ini.core.md#ini.default-charset) і, якщо буде виявлено некоректну послідовність байт для даного кодування, то весь рядок буде визнаний непридатним і результатом буде рядок нульової довжини. При використанні цього фільтра як фільтр за замовчуванням, ознайомтеся з попередженням нижче про встановлення прапорів за промовчанням у 0. |
| **`FILTER_SANITIZE_STRING`** | "string" | **`FILTER_FLAG_NO_ENCODE_QUOTES`** **`FILTER_FLAG_STRIP_LOW`** **`FILTER_FLAG_STRIP_HIGH`** **`FILTER_FLAG_STRIP_BACKTICK`** **`FILTER_FLAG_ENCODE_LOW`** **`FILTER_FLAG_ENCODE_HIGH`** **`FILTER_FLAG_ENCODE_AMP`** | Видаляє теги та кодує подвійні та одинарні лапки, при необхідності видаляє або кодує спеціальні символи. Кодування лапок можна вимкнути, встановивши **`FILTER_FLAG_NO_ENCODE_QUOTES`**. (Оголошено *застарілим*, починаючи з PHP 8.1.0, використовуйте замість нього функцію [htmlspecialchars()](function.htmlspecialchars.md) |
| **`FILTER_SANITIZE_STRIPPED`** | "stripped" |  | Псевдонім фільтра "string". (Оголошено *застарілим*, починаючи з PHP 8.1.0, використовуйте замість нього функцію [htmlspecialchars()](function.htmlspecialchars.md) |
| **`FILTER_SANITIZE_URL`** | "url" |  | Видаляє всі символи, окрім букв, цифр і \`\`$-\_.+!\*'(),{} |
| **`FILTER_UNSAFE_RAW`** | "unsaferaw" | **`FILTER_FLAG_STRIP_LOW`** **`FILTER_FLAG_STRIP_HIGH`** **`FILTER_FLAG_STRIP_BACKTICK`** **`FILTER_FLAG_ENCODE_LOW`** **`FILTER_FLAG_ENCODE_HIGH`** **`FILTER_FLAG_ENCODE_AMP`** | Не діє, при необхідності видаляє або кодує спеціальні символи. Цей фільтр є псевдонімом **`FILTER_DEFAULT`** |

**Увага**

При використанні одного з цих фільтрів як фільтр за промовчанням або через ваш ini-файл, або через конфігурацію веб-сервера, прапори за промовчанням встановлені в значення **`FILTER_FLAG_NO_ENCODE_QUOTES`**. Вам необхідно явно встановити параметр filter.defaultflags значення 0 для наявності порожніх лапок за замовчуванням. Наприклад:

**Приклад #1 Налаштування стандартного фільтра для роботи аналогічно функції htmlspecialchars**

```php
filter.default = full_special_chars
filter.default_flags = 0
```

### список змін

| Версия | Описание |
| --- | --- |
|  | Вилучена **`FILTER_SANITIZE_MAGIC_QUOTES`** |
|  | Додана **`FILTER_SANITIZE_ADD_SLASHES`** для заміни **`FILTER_SANITIZE_MAGIC_QUOTES`** |
|  | **`FILTER_SANITIZE_MAGIC_QUOTES`** оголошено застарілою. |
