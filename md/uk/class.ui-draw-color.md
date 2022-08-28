Подання кольору

-   [« UI\\Draw\\Matrix::translate](ui-draw-matrix.translate.html)
    
-   [UI\\Draw\\Color::\_\_construct »](ui-draw-color.construct.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   Подання кольору
    

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

-   [UI\\Draw\\Color::\_\_construct](ui-draw-color.construct.html) — Створити новий об'єкт Color
-   [UI\\Draw\\Color::getChannel](ui-draw-color.getchannel.html) - Управління кольором
-   [UI\\Draw\\Color::setChannel](ui-draw-color.setchannel.html) - Управління кольором