---
navigation:
  - function.imap-setflag-full.md: « imapsetflagfull
  - function.imap-status.md: imapstatus »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapsort
---
# imapsort

(PHP 4, PHP 5, PHP 7, PHP 8)

imapsort — Отримати та відсортувати повідомлення

### Опис

```methodsynopsis
imap_sort(    IMAP\Connection $imap,    int $criteria,    bool $reverse,    int $flags = 0,    ?string $search_criteria = null,    ?string $charset = null): array|false
```

Отримує та сортує номери повідомлень відповідно до заданих параметрів.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

`criteria`

Одне (і лише одне) з наступних значень:

-   **`SORTDATE`** - сортувати за датою
-   **`SORTARRIVAL`** - дата отримання
-   **`SORTFROM`** - за першою адресою у полі From
-   **`SORTSUBJECT`** - на тему листа
-   **`SORTTO`** - на першу адресу в полі To
-   **`SORTCC`** - за першою адресою в полі cc
-   **`SORTSIZE`** - за розміром повідомлення

`reverse`

Визначає сортування у зворотному порядку.

`flags`

Параметр `flags` задається бітовою маскою однієї або кількох констант:

-   **`SE_UID`** - повертати UID, а не номери повідомлень
-   **`SE_NOPREFETCH`** - не отримувати знайдені повідомлення

`search_criteria`

Рядок з пошуковим критерієм у форматі IMAP2. Докладніше дивіться в описі функції [imapsearch()](function.imap-search.md)

`charset`

Кодування MIME для використання під час сортування рядків.

### Значення, що повертаються

Повертає масив номерів повідомлень, відсортованих відповідно до заданих параметрів або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `reverse` тепер є логічним типом (Bool) замість цілого числа (int). |
|  | `search_criteria` і `charset` тепер є nullable. |
