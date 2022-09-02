---
navigation:
  - function.mb-ereg-search-init.md: « mberegsearchinit
  - function.mb-ereg-search-regs.md: мбeregsearchregs »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбeregsearchpos
---
# мбeregsearchpos

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

мбeregsearchpos — Повертає позицію і довжину збігу з регулярним виразом ділянки багатобайтового рядка

### Опис

```methodsynopsis
mb_ereg_search_pos(?string $pattern = null, ?string $options = null): array|false
```

Повертає позицію і довжину ділянки, що збіглася з регулярним виразом заздалегідь визначеного багатобайтного рядка.

Рядок для пошуку задається функцією [мбeregsearchinit()](function.mb-ereg-search-init.md). Якщо вона не задавалася, буде використано рядок, заданий раніше.

### Список параметрів

`pattern`

Шаблон, текст регулярного виразу.

`options`

Опція пошуку. Детальніше дивіться [мбregexsetoptions()](function.mb-regex-set-options.md)

### Значення, що повертаються

Масив (array) містить два елементи. Перший елемент - усунення в байтах, з якого починається збіг щодо початку шуканого рядка, і другий елемент - довжина збігу в байтах.

У разі виникнення помилки повертається **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `pattern` і `options` тепер допускають значення null. |

### Примітки

> **Зауваження**
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [мбregexencoding()](function.mb-regex-encoding.md)

### Дивіться також

-   [мбregexencoding()](function.mb-regex-encoding.md) - Встановлює/отримує поточне кодування для багатобайтового регулярного виразу
-   [мбeregsearchinit()](function.mb-ereg-search-init.md) - Ініціалізація пошуку відповідностей регулярному виразу багатобайтовим рядком та текстом регулярного вираження
