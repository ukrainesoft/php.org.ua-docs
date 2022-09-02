---
navigation:
  - class.parallel-channel.md: « parallelChannel
  - parallel-channel.make.md: 'parallelChannel::make »'
  - index.md: PHP Manual
  - class.parallel-channel.md: parallelChannel
title: 'parallelChannel::construct'
---
# parallelChannel::construct

parallelChannel::construct - Конструктор класу Channel

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
