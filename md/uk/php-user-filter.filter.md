---
navigation:
  - class.php-user-filter.md: « php\_user\_filter
  - php-user-filter.onclose.md: 'php\_user\_filter::onClose »'
  - index.md: PHP Manual
  - class.php-user-filter.md: php\_user\_filter
title: 'php\_user\_filter::filter'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# php\_user\_filter::filter

(PHP 5, PHP 7, PHP 8)

php\_user\_filter::filter — Викликається, як тільки застосовується фільтр

### Опис

```methodsynopsis
public php_user_filter::filter(    resource $in,    resource $out,    int &$consumed,    bool $closing): int
```

Цей метод викликається щоразу, коли дані читаються з приєднаного потоку або записуються до нього (такими функціями, як [fread()](function.fread.md) або [fwrite()](function.fwrite.md)

### Список параметрів

`in`

`in` - Ресурс, що вказує на `bucket brigade`яка містить один або кілька об'єктів `bucket` містять дані, що фільтруються.

`out`

`out` - Ресурс, що вказує на інший об'єкт `bucket brigade`, в який будуть розміщені модифіковані бакети.

`consumed`

`consumed`, який має *завжди* передаватися за посиланням, має збільшуватися розмір даних, які фільтр читає і змінює. У більшості випадків це означає, що ви самі збільшуватимете значення `consumed`на`$bucket->datalen` для кожного `$bucket`

`closing`

Якщо потік закривається (отже, це останній фільтр у ланцюжку), аргумент `closing`примет значение\*\*`true`\*\*

### Значення, що повертаються

Метод**filter()** повинен повертати одне із трьох значень.

| Возвращаемое значение | Опис |
| --- | --- |
| **`PSFS_PASS_ON`** | Фільтр відпрацював успішно, дані доступні через аргумент `out` `bucket brigade` |
| **`PSFS_FEED_ME`** | Фільтр відпрацював успішно, проте доступних для виведення даних немає. Потрібні дані з потоку або попереднього фільтра. |
| **`PSFS_ERR_FATAL`**(за замовчуванням) | Фільтр викликав помилку, що не обробляється, і не може продовжити виконання. |
