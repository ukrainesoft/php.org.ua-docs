---
navigation:
  - event.examples.md: « Приклади
  - event.persistence.md: Про постійні (persistent) події »
  - index.md: PHP Manual
  - book.event.md: Event
title: Прапори подій
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Прапори подій

Флаг\*\*`Event::READ`\*\* вказує подію, яка стає активною, коли наданий файл (частіше потоковий ресурс або сокет) готовий до читання.

Флаг\*\*`Event::WRITE`\*\* вказує подію, яка стає активною, коли наданий файл (частіше потоковий ресурс або сокет) готовий до запису.

Флаг\*\*`Event::SIGNAL`\*\* вказують для реалізації відстеження системних сигналів. Докладніше про це наведено в розділі «Створення подій для сигналів».

Флаг\*\*`Event::TIMEOUT`\*\* вказує подію, яка стає активною після закінчення часу очікування. Прапор **`Event::TIMEOUT`** ігнорується при створенні події: його можна встановити за *додаванні*. Він задається в аргументі `$what` callback-функції, якщо сталася подія цього.

Рекомендовано также прочитать[» Fast portable non-blocking network programming with Libevent, Working with events, Event flags](http://www.wangafu.net/~nickm/libevent-book/Ref4_event.md#_the_event_flags)
