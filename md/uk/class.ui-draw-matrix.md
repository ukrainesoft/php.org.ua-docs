---
navigation:
  - ui-draw-path.newfigurewitharc.md: '« UIDrawPath::newFigureWithArc'
  - ui-draw-matrix.invert.md: 'ОЙDrawMatrix::invert »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Матриця малювання
---
# Матриця малювання

(UI 0.9.9)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class UI\Draw\Matrix
     
     {


    /* Методы */
    
   public invert()
public isInvertible(): bool
public multiply(UI\Draw\Matrix $matrix): UI\Draw\Matrix
public rotate(UI\Point $point, float $amount)
public scale(UI\Point $center, UI\Point $point)
public skew(UI\Point $point, UI\Point $amount)
public translate(UI\Point $point)

   }
```

## Зміст

-   [ОЙDrawMatrix::invert](ui-draw-matrix.invert.md) - Інвертувати матрицю
-   [ОЙDrawMatrix::isInvertible](ui-draw-matrix.isinvertible.md) — Визначення, чи інвертовано матрицю
-   [ОЙDrawMatrix::multiply](ui-draw-matrix.multiply.md) - Помножити матрицю
-   [ОЙDrawMatrix::rotate](ui-draw-matrix.rotate.md) - Перевернути матрицю
-   [ОЙDrawMatrix::scale](ui-draw-matrix.scale.md) - Масштабувати матрицю
-   [ОЙDrawMatrix::skew](ui-draw-matrix.skew.md) - Нахилити матрицю
-   [ОЙDrawMatrix::translate](ui-draw-matrix.translate.md) - Перекласти матрицю
