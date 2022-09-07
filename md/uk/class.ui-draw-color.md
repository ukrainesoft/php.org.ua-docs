---
navigation:
  - ui-draw-matrix.translate.md: '« UIDrawMatrix::translate'
  - ui-draw-color.construct.md: 'ОЙDrawColor::construct »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Подання кольору
---
# Подання кольору

(UI 0.9.9)

## Вступ

Є кольори RGBA, окремі канали доступні через загальнодоступні властивості.

## Огляд класів

```classsynopsis



    
     
      class UI\Draw\Color
     
     {

    /* Константы */
    
     const
     int
      Red;

    const
     int
      Green;

    const
     int
      Blue;

    const
     int
      Alpha;


    /* Свойства */
    public
      $r;

    public
      $g;

    public
      $b;

    public
      $a;


    /* Конструктор */
    
   public __construct(UI\Draw\Color $color = ?)
public __construct(int $color = ?)


    /* Методы */
    public getChannel(int $channel): float
public setChannel(int $channel, float $value): void

   }
```

## Властивості

р

Забезпечує доступ до червоного каналу

г

Забезпечує доступ до зеленого каналу

в

Забезпечує доступ до синього каналу

а

Забезпечує доступ до альфа-каналу

## Обумовлені константи

**`UI\Draw\Color::Red`**

Визначає червоний канал

**`UI\Draw\Color::Green`**

Визначає зелений канал

**`UI\Draw\Color::Blue`**

Визначає синій канал

**`UI\Draw\Color::Alpha`**

Визначає альфа-канал

## Зміст

-   [ОЙDrawColor::construct](ui-draw-color.construct.md) — Створити новий об'єкт Color
-   [ОЙDrawColor::getChannel](ui-draw-color.getchannel.md) - Управління кольором
-   [ОЙDrawColor::setChannel](ui-draw-color.setchannel.md) - Управління кольором
