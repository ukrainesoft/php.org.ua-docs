---
navigation:
  - ev.backend.md: '« Ev::backend'
  - ev.embeddablebackends.md: 'Ev::embeddableBackends »'
  - index.md: PHP Manual
  - class.ev.md: Ev
title: 'Ev::depth'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ev::depth

(PECL ev >= 0.2.0)

Ev::depth — Здобути глибину рекурсії

### Опис

```methodsynopsis
final
   public
   static
   Ev::depth(): int
```

Кількість запусків [Ev::run()](ev.run.md) мінус кількість нормальних виходів [Ev::run()](ev.run.md), Іншими словами, глибина рекурсії. Поза [Ev::run()](ev.run.md) це число буде рівним . У callback-функції воно буде рівним , якщо [Ev::run()](ev.run.md) не викликалася рекурсивно (чи іншому потоці), інакше воно буде більше.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**ev\_depth()** повертає глибину рекурсії циклу за умовчанням.

### Дивіться також

-   [Ev::iteration()](ev.iteration.md) \- Отримати кількість проведених опитувань циклу за умовчанням щодо нових подій
