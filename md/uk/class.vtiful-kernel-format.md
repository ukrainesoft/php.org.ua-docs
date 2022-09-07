---
navigation:
  - vtiful-kernel-excel.setRow.md: '« VtifulKernelExcel::setRow'
  - vtiful-kernel-format.align.md: 'VtifulKernelFormat::align »'
  - index.md: PHP Manual
  - book.xlswriter.md: XLSWriter
title: Клас VtifulKernelФормат
---
# Клас VtifulKernelФормат

(PECL xlswriter >= 1.2.1)

## Вступ

Повертає об'єкт форматування комірки

## Огляд класів

```classsynopsis



    
     
      class Vtiful\Kernel\Format
     
     {


    /* Константы */
    
     const
     int
      FORMAT_ALIGN_LEFT = 1;

    const
     int
      FORMAT_ALIGN_CENTER = 2;

    const
     int
      FORMAT_ALIGN_RIGHT = 3;

    const
     int
      FORMAT_ALIGN_FILL = 4;

    const
     int
      FORMAT_ALIGN_JUSTIFY = 5;

    const
     int
      FORMAT_ALIGN_CENTER_ACROSS = 6;

    const
     int
      FORMAT_ALIGN_DISTRIBUTED = 7;

    const
     int
      FORMAT_ALIGN_VERTICAL_TOP = 8;

    const
     int
      FORMAT_ALIGN_VERTICAL_BOTTOM = 9;

    const
     int
      FORMAT_ALIGN_VERTICAL_CENTER = 10;

    const
     int
      FORMAT_ALIGN_VERTICAL_JUSTIFY = 11;

    const
     int
      FORMAT_ALIGN_VERTICAL_DISTRIBUTED = 12;

    const
     int
      UNDERLINE_SINGLE = 1;

    const
     int
      UNDERLINE_DOUBLE = 2;

    const
     int
      UNDERLINE_SINGLE_ACCOUNTING = 3;

    const
     int
      UNDERLINE_DOUBLE_ACCOUNTING = 4;


    /* Методы */
    
   public align(resource $handle, int $style)
public bold(resource $handle)
public italic(resource $handle)
public underline(resource $handle, int $style)


   }
```

## Обумовлені константи

**`Vtiful\Kernel\Format::FORMAT_ALIGN_LEFT`**

**`Vtiful\Kernel\Format::FORMAT_ALIGN_CENTER`**

**`Vtiful\Kernel\Format::FORMAT_ALIGN_RIGHT`**

**`Vtiful\Kernel\Format::FORMAT_ALIGN_FILL`**

**`Vtiful\Kernel\Format::FORMAT_ALIGN_JUSTIFY`**

**`Vtiful\Kernel\Format::FORMAT_ALIGN_CENTER_ACROSS`**

**`Vtiful\Kernel\Format::FORMAT_ALIGN_DISTRIBUTED`**

**`Vtiful\Kernel\Format::FORMAT_ALIGN_VERTICAL_TOP`**

**`Vtiful\Kernel\Format::FORMAT_ALIGN_VERTICAL_BOTTOM`**

**`Vtiful\Kernel\Format::FORMAT_ALIGN_VERTICAL_CENTER`**

**`Vtiful\Kernel\Format::FORMAT_ALIGN_VERTICAL_JUSTIFY`**

**`Vtiful\Kernel\Format::FORMAT_ALIGN_VERTICAL_DISTRIBUTED`**

**`Vtiful\Kernel\Format::UNDERLINE_SINGLE`**

**`Vtiful\Kernel\Format::UNDERLINE_DOUBLE`**

**`Vtiful\Kernel\Format::UNDERLINE_SINGLE_ACCOUNTING`**

**`Vtiful\Kernel\Format::UNDERLINE_DOUBLE_ACCOUNTING`**

## Зміст

-   [VtifulKernelFormat::align](vtiful-kernel-format.align.md) - Вирівнювання
-   [VtifulKernelFormat::bold](vtiful-kernel-format.bold.md) - Напівжирний
-   [VtifulKernelFormat::italic](vtiful-kernel-format.italic.md) - Курсив
-   [VtifulKernelFormat::underline](vtiful-kernel-format.underline.md) - Підкреслений
