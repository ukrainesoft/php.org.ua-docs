---
navigation:
  - evidle.createstopped.md: '« EvIdle::createStopped'
  - evio.construct.md: 'EvIo::construct »'
  - index.md: PHP Manual
  - book.ev.md: Єв
title: Клас EvIo
---
# Клас EvIo

(PECL ev >= 0.2.0)

## Вступ

Спостерігачі **EvIo** перевіряють, чи є файл, сокет або потік, що перетворюється на числовий дескриптор файлу, доступним на читання або запис при кожній ітерації подійного циклу, або, якщо точніше, коли читання не заблокує процес, а запис зможе бути зроблено. Така поведінка називається *перемикання рівня (level-triggering)*, тому, що події будуть створюватися весь час, поки зберігається відстежуваний стан. Для припинення створення подій потрібно просто зупинити спостерігача.

Кількість таких спостерігачів для одного файлового дескриптора `fd` НЕ обмежено. Бажано, але не обов'язково встановити для файлового дескриптора неблокуючий режим.

Інший момент, який необхідно пам'ятати, це те, що завжди існує можливість помилкового спрацьовування. Наприклад **`Ev::READ`** викличе callback-функцію, але в той же час файл заблокується під запитом *read()*. У таку ситуацію дуже легко потрапити і тому рекомендується завжди використовувати неблокуючий ввод/вывод. Повернення *read()* додаткового **`EAGAIN`** набагато краще, ніж "зависання" програми в очікуванні даних.

Якщо з якихось причин неможливо використати `fd` в неблокуючому режимі, то є сенс додатково перевіряти, чи доступний файл читання в даний конкретний момент. Хтось додатково використовує **`SIGALRM`** та внутрішній таймер для перевірки, що блокування не вічне.

Намагайтеся завжди використовувати режим, що не блокує.

## Огляд класів

```classsynopsis

     
    
    
    
     
      class EvIo
     
     
      extends
       EvWatcher
     
     {
    
    /* Свойства */
    
     public
      $fd;

    public
      $events;

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
    mixed
     $fd
   ,    
    int
     $events
   ,    
    callable
     $callback
   ,    
    mixed
     $data
    = ?,    
    int
     $priority
    = ?)

    final
   public
   static
   createStopped(    
    mixed
     $fd
   ,    
    int
     $events
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
   ): EvIo
public
   set(
    mixed
     $fd
   , 
    int
     $events
   ): void

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

фд

events

## Зміст

-   [EvIo::construct](evio.construct.md) - Створює об'єкт спостерігач EvIo
-   [EvIo::createStopped](evio.createstopped.md) — Створює зупинений об'єкт спостерігача EvIo
-   [EvIo::set](evio.set.md) - Конфігурування спостерігача
