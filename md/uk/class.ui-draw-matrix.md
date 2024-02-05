---
navigation:
  - ui-draw-path.newfigurewitharc.md: '« UI\\Draw\\Path::newFigureWithArc'
  - ui-draw-matrix.invert.md: 'UI\\Draw\\Matrix::invert »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Матриця малювання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   [UI\\Draw\\Matrix::invert](ui-draw-matrix.invert.md) \- Інвертувати матрицю
-   [UI\\Draw\\Matrix::isInvertible](ui-draw-matrix.isinvertible.md)— Визначення, чи інвертовано матрицю
-   [UI\\Draw\\Matrix::multiply](ui-draw-matrix.multiply.md) \- Помножити матрицю
-   [UI\\Draw\\Matrix::rotate](ui-draw-matrix.rotate.md) \- Перевернути матрицю
-   [UI\\Draw\\Matrix::scale](ui-draw-matrix.scale.md) \- Масштабувати матрицю
-   [UI\\Draw\\Matrix::skew](ui-draw-matrix.skew.md) \- Нахилити матрицю
-   [UI\\Draw\\Matrix::translate](ui-draw-matrix.translate.md) \- Перекласти матрицю
