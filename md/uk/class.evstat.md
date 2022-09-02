---
navigation:
  - evsignal.set.md: '« EvSignal::set'
  - evstat.attr.md: 'EvStat::attr »'
  - index.md: PHP Manual
  - book.ev.md: Єв
title: Клас EvStat
---
# Клас EvStat

(PECL ev >= 0.2.0)

## Вступ

**EvStat** спостерігає за зміною атрибутів об'єкта заданим шляхом у файловій системі. Це досягається шляхом регулярного запуску *стати()* для цього шляху (або шляхом отримання сигналу про зміну від операційної системи) та порівняння отриманих даних з результатами попереднього виклику. У разі виявлення зміни атрибутів викликається callback-функція.

Шлях не обов'язково має існувати насправді. Зміна статусу з "шлях існує" на "шлях не існує" - це така ж зміна, як і будь-яке інше. Стан "шлях не існує" визначається за значенням **`'nlink'`** рівним 0 (яке повертається методом [EvStat::attr()](evstat.attr.md)

Шлях не повинен закінчуватися слішем або містити спеціальні компоненти, такі як **`'.'`** або **`..`**. Шлях має бути абсолютним. Якщо задати відносний шлях і змінити робочий каталог, поведінка буде невизначеною.

Оскільки немає інтерфейсу сповіщення про зміни, що переноситься, переносна реалізація просто викликає *стати()* через рівні проміжки часу і дивиться, чи не змінилося чогось. Тому рекомендується ставити інтервал опитування. Якщо інтервал опитування заданий рівним **`0.0`** (що вкрай рекомендується), то використовуватиметься значення за замовчуванням (якого ніхто не знає, але передбачається, що десь близько 5 секунд, але при цьому може динамічно змінюватися) . *libev* має обмеження на мінімальне значення інтервалу, яке зараз дорівнює приблизно \*\*`0.1`\*\*Але такий інтервал - це стрілянина з гармати по горобцях.

Не рекомендується використовувати велику кількість одночасно працюючих спостерігачів **EvStat**оскільки це може сильно вплинути на споживання ресурсів у зв'язку з використанням механізмів оповіщення операційної системи.

## Огляд класів

```classsynopsis

     
    
    
    
     
      class EvStat
     
     
      extends
       EvWatcher
     
     {
    
    /* Свойства */
    
     public
      $path;

    public
      $interval;

    /* Наследуемые свойства */
    public
      $is_active;
public
      $data;
public
      $is_pending;
public
      $priority;

    /* Методы */
    
   public
   __construct(    
    string
     $path
   ,    
    float
     $interval
   ,    
    callable
     $callback
   ,    
    mixed
     $data
     = null
   ,    
    int
     $priority
     = 0
   )

    public
   attr(): array
final
   public
   static
   createStopped(    
    string
     $path
   ,    
    float
     $interval
   ,    
    callable
     $callback
   ,    
    mixed
     $data
     = null
   ,    
    int
     $priority
     = 0
   ): void
public
   prev(): void
public
   set(
    string
     $path
   , 
    float
     $interval
   ): void
public
   stat(): bool

    /* Наследуемые методы */
    public
   EvWatcher::clear(): int
public
   EvWatcher::feed(
    int
     $revents
   ): void
public
   EvWatcher::getLoop(): EvLoop
public
   EvWatcher::invoke(
    int
     $revents
   ): void
public
   EvWatcher::keepalive(
    bool
     $value
    = ?): bool
public
   EvWatcher::setCallback(
    callable
     $callback
   ): void
public
   EvWatcher::start(): void
public
   EvWatcher::stop(): void

   }
```

## Властивості

interval

*Тільки читання*. Показує, наскільки часто відбуваються опитування статусу і зазвичай одно **`0.0`**, що дозволяє *libev* самостійно визначати інтервал.

path

*Тільки читання*. Шлях, для якого відстежуються зміни.

## Зміст

-   [EvStat::attr](evstat.attr.md) — Повертає значення, нещодавно виявлені Ev
-   [EvStat::construct](evstat.construct.md) - Створює об'єкт спостерігача EvStat
-   [EvStat::createStopped](evstat.createstopped.md) - Створює зупинений об'єкт спостерігача EvStat
-   [EvStat::prev](evstat.prev.md) — Повертає попередній набір значень, які повертаються EvStat::attr
-   [EvStat::set](evstat.set.md) — Налаштовує спостерігача
-   [EvStat::stat](evstat.stat.md) - Ініціює виклик статистики
