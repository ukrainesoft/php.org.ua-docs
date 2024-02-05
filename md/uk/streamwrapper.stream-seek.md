---
navigation:
  - streamwrapper.stream-read.md: '« streamWrapper::stream\_read'
  - streamwrapper.stream-set-option.md: 'streamWrapper::stream\_set\_option »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::stream\_seek'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::stream\_seek

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::stream\_seek — Переміщення на задану позицію у потоці

### Опис

```methodsynopsis
public streamWrapper::stream_seek(int $offset, int $whence  = SEEK_SET): bool
```

Цей метод викликається у процесі виконання [fseek()](function.fseek.md)

Позицію читання/запису в потоці необхідно оновлювати відповідно до аргументів `offset`и`whence`

### Список параметрів

`offset`

Зміщення у потоці, на яке потрібно переміститися.

`whence`

Можливі значення:

-   \*\*`SEEK_SET`\*\*- Переміститися на позицію`offset`байт от начала файла.
-   \*\*`SEEK_CUR`\*\*- Переміститися на`offset`байт щодо поточної позиції.
-   \*\*`SEEK_END`\*\*- Переміститися на позицію`offset`байт від кінця файлу.

> **Зауваження**: Поточна реалізація ніколи не встановлює для `whence`значение\*\*`SEEK_CUR`\*\*; натомість такі пошуки внутрішньо перетворюються на пошуки **`SEEK_SET`**

### Значення, що повертаються

Повертає **`true`**, если позиция обновлена,**`false`** в інших випадках.

### Примітки

> **Зауваження** :
> 
> Якщо не реалізований, як значення, що повертається, приймається **`false`**

> **Зауваження** :
> 
> У разі успішного виконання [streamWrapper::stream\_tell()](streamwrapper.stream-tell.md) буде викликано відразу після того, як **streamWrapper::stream\_seek()** відпрацює. Якщо виконання [streamWrapper::stream\_tell()](streamwrapper.stream-tell.md) завершиться невдачею, то викликаючу функцію буде повернуто значення **`false`**

> **Зауваження** :
> 
> Не всі операції переміщення у потоці призведуть до виклику цієї функції. У PHP за замовчуванням включено буферизацію потоків (дивіться також [stream\_set\_read\_buffer()](function.stream-set-read-buffer.md)), тому переміщення в потоці може означати лише переміщення покажчика буфері.

### Дивіться також

-   [fseek()](function.fseek.md) \- Встановлює зміщення у файловому покажчику
