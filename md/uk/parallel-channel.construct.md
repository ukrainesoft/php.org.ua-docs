---
navigation:
  - class.parallel-channel.md: « parallel\\Channel
  - parallel-channel.make.md: 'parallel\\Channel::make »'
  - index.md: PHP Manual
  - class.parallel-channel.md: parallel\\Channel
title: 'parallel\\Channel::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Channel::\_\_construct

(1.1.0)

parallel\\Channel::\_\_construct - Конструктор класу Channel

### Опис

```methodsynopsis
public parallel\Channel::__construct()
```

Створює анонімний небуферизований канал

```methodsynopsis
public parallel\Channel::__construct(int $capacity)
```

Створює анонімний буферизований канал із заданою ємністю.

### Список параметрів

`capacity`

Може бути Channel::Infinite або позитивним цілим числом.
