---
navigation:
  - class.ev.md: « Ev
  - ev.depth.md: 'Ev::depth »'
  - index.md: PHP Manual
  - class.ev.md: Єв
title: 'Ev::backend'
---
# Ev::backend

(PECL ev >= 0.2.0)

Ev::backend - Повертає ціле число, що описує бекенд, що використовується libev

### Опис

```methodsynopsis
final
   public
   static
   Ev::backend(): int
```

Повертає ціле число, що описує бекенд, що використовується *libev*. Дивіться [Прапори бекенда](class.ev.html#ev.constants.watcher-backends)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ціле число (бітова маска), що описує бекенд, що використовується *libev*

### Дивіться також

-   [EvEmbed](class.evembed.md)
-   [Ev::embeddableBackends()](ev.embeddablebackends.md) - Повертає набір бекендів, які можна вбудувати в інші цикли подій
-   [Ev::recommendedBackends()](ev.recommendedbackends.md) - Отримати бітову маску рекомендованих бекендів для даної платформи
-   [Ev::supportedBackends()](ev.supportedbackends.md) - Повертає набір бекендів, які підтримуються поточною конфігурацією libev
-   [Прапори бекенда](class.ev.html#ev.constants.watcher-backends)
