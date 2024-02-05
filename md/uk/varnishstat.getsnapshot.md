---
navigation:
  - varnishstat.construct.md: '« VarnishStat::\_\_construct'
  - class.varnishlog.md: VarnishLog »
  - index.md: PHP Manual
  - class.varnishstat.md: VarnishStat
title: 'VarnishStat::getSnapshot'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# VarnishStat::getSnapshot

(PECL varnish >= 0.3)

VarnishStat::getSnapshot — Отримати фотографію статистики поточного екземпляра varnish

### Опис

```methodsynopsis
public VarnishStat::getSnapshot(): array
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив зі знімком varnish статистики. Ключі масиву ідентичні ключам у команді varnishstat.
