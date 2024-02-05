---
navigation:
  - streamwrapper.stream-eof.md: '« streamWrapper::stream\_eof'
  - streamwrapper.stream-lock.md: 'streamWrapper::stream\_lock »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::stream\_flush'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::stream\_flush

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::stream\_flush - Скидає висновок

### Опис

```methodsynopsis
public streamWrapper::stream_flush(): bool
```

Цей метод викликається у процесі виконання [fflush()](function.fflush.md), якщо потік закривається маючи незрушені дані, записані до нього раніше.

Якщо в потоці є кешовані і ще невикористані дані, у цьому методі місце передати їх на нижчий рівень.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повинен повертати \*\*`true`\*\*якщо кешовані дані успішно збережені (або їх взагалі немає), або \*\*`false`\*\*якщо дані не можуть бути збережені.

### Примітки

> **Зауваження** :
> 
> Якщо метод не реалізований, як значення, що повертається, належить **`false`**

### Дивіться також

-   [fflush()](function.fflush.md) \- скидає буфер виведення у файл
