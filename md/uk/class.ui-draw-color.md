---
navigation:
  - ui-draw-matrix.translate.md: '« UI\\Draw\\Matrix::translate'
  - ui-draw-color.construct.md: 'UI\\Draw\\Color::\_\_construct »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Подання кольору
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

r

Забезпечує доступ до червоного каналу

g

Забезпечує доступ до зеленого каналу

b

Забезпечує доступ до синього каналу

a

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

-   [UI\\Draw\\Color::\_\_construct](ui-draw-color.construct.md)— Створити новий об'єкт Color
-   [UI\\Draw\\Color::getChannel](ui-draw-color.getchannel.md) \- Управління кольором
-   [UI\\Draw\\Color::setChannel](ui-draw-color.setchannel.md) \- Управління кольором
