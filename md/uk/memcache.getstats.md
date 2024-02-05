---
navigation:
  - memcache.getserverstatus.md: '« Memcache::getServerStatus'
  - memcache.getversion.md: 'Memcache::getVersion »'
  - index.md: PHP Manual
  - class.memcache.md: Memcache
title: 'Memcache::getStats'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcache::getStats

(PECL memcache >= 0.2.0)

Memcache::getStats — Отримати статистику сервера

### Опис

```methodsynopsis
Memcache::getStats(string $type = ?, int $slabid = ?, int $limit = 100): array|false
```

**Memcache::getStats()** повертає асоціативний масив, який містить статистику сервера. Ключі масиву відповідають параметрам статистики, а значення – значенням параметрів. Також можна використовувати функцію **memcache\_get\_stats()**

### Список параметрів

`type`

Тип статистики для отримання. Коректні значення: reset, malloc, maps, cachedump, slabs, items, sizes. Відповідно до специфікації протоколу memcached, ці додаткові аргументи "можуть бути змінені для зручності розробників memcache".

`slabid`

Використовується спільно з `type` для вказівки, з якого slab-файлу робити вивантаження. Використовується тільки для налагодження. Команда cachedump намагається запустити сервер і повинна використовуватися лише для налагодження.

`limit`

Используется вместе с`type` для обмеження кількості записів, що витягуються.

### Значення, що повертаються

Повертає асоціативний масив, що містить статистику сервера або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [Memcache::getVersion()](memcache.getversion.md) \- Повернути версію сервера
-   [Memcache::getExtendedStats()](memcache.getextendedstats.md) \- Отримати статистику з усіх серверів у пулі
