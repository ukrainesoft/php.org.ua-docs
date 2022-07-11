- [« Vtiful\Kernel\Excel::setRow](vtiful-kernel-excel.setRow.md)
- [Vtiful\Kernel\Format::align »](vtiful-kernel-format.align.md)

- [PHP Manual](index.md)
- [XLSWriter](book.xlswriter.md)
- Клас Vtiful\Kernel\Format

# Клас Vtiful\Kernel\Format

(PECL xlswriter \>= 1.2.1)

## Вступ

Повертає об'єкт форматування комірки

## Огляд класів

class **Vtiful\Kernel\Format** {

/\* Константи \*/

const int `FORMAT_ALIGN_LEFT` = 1;

const int `FORMAT_ALIGN_CENTER` = 2;

const int `FORMAT_ALIGN_RIGHT` = 3;

const int `FORMAT_ALIGN_FILL` = 4;

const int `FORMAT_ALIGN_JUSTIFY` = 5;

const int `FORMAT_ALIGN_CENTER_ACROSS` = 6;

const int `FORMAT_ALIGN_DISTRIBUTED` = 7;

const int `FORMAT_ALIGN_VERTICAL_TOP` = 8;

const int `FORMAT_ALIGN_VERTICAL_BOTTOM` = 9;

const int `FORMAT_ALIGN_VERTICAL_CENTER` = 10;

const int `FORMAT_ALIGN_VERTICAL_JUSTIFY` = 11;

const int `FORMAT_ALIGN_VERTICAL_DISTRIBUTED` = 12;

const int `UNDERLINE_SINGLE` = 1;

const int `UNDERLINE_DOUBLE` = 2;

const int `UNDERLINE_SINGLE_ACCOUNTING` = 3;

const int `UNDERLINE_DOUBLE_ACCOUNTING` = 4;

/\* Методи \*/

public [align](vtiful-kernel-format.align.md)(resource `$handle`, int
`$style`)

public [bold](vtiful-kernel-format.bold.md)(resource `$handle`)

public [italic](vtiful-kernel-format.italic.md)(resource `$handle`)

public [underline](vtiful-kernel-format.underline.md)(resource
`$handle`, int `$style`)

}

## Зумовлені константи

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

- [Vtiful\Kernel\Format::align](vtiful-kernel-format.align.md) -
Вирівнювання
- [Vtiful\Kernel\Format::bold](vtiful-kernel-format.bold.md) -
Напівжирний
- [Vtiful\Kernel\Format::italic](vtiful-kernel-format.italic.md) -
Курсив
- [Vtiful\Kernel\Format::underline](vtiful-kernel-format.underline.md)
- Підкреслений
