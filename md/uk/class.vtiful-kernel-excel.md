---
navigation:
  - xlswriter.constants.md: « Обумовлені константи
  - vtiful-kernel-excel.addSheet.md: 'VtifulKernelExcel::addSheet »'
  - index.md: PHP Manual
  - book.xlswriter.md: XLSWriter
title: Клас VtifulKernelExcel
---
# Клас VtifulKernelExcel

(PECL xlswriter >= 1.2.1)

## Вступ

Створює файли xlsx із заданими осередками

## Огляд класів

```classsynopsis


    
    
     
      class Vtiful\Kernel\Excel
     
     {
    

    /* Методы */
    
   public __construct(array $config)

    public addSheet(string $sheetName)
public autoFilter(string $scope)
public constMemory(string $fileName, string $sheetName = ?)
public data(array $data)
public fileName(string $fileName, string $sheetName = ?)
public getHandle()
public header(array $headerData)
public insertFormula(int $row, int $column, string $formula)
public insertImage(int $row, int $column, string $localImagePath)
public insertText(    int $row,    int $column,    stringintdouble $data,    string $format = ?)
public mergeCells(string $scope, string $data)
public output()
public setColumn(string $range, float $width, resource $format = ?)
public setRow(string $range, float $height, resource $format = ?)


   }
```

## Зміст

-   [VtifulKernelExcel::addSheet](vtiful-kernel-excel.addSheet.md) - Додати лист
-   [VtifulKernelExcel::autoFilter](vtiful-kernel-excel.autoFilter.md) - Додати автофільтр
-   [VtifulKernelExcel::constMemory](vtiful-kernel-excel.constMemory.md) - Кількість пам'яті
-   [VtifulKernelExcel::construct](vtiful-kernel-excel.construct.md) - Конструктор
-   [VtifulKernelExcel::data](vtiful-kernel-excel.data.md) - Записати дані
-   [VtifulKernelExcel::fileName](vtiful-kernel-excel.filename.md) — Створити назву файлу
-   [VtifulKernelExcel::getHandle](vtiful-kernel-excel.getHandle.md) - Отримати дескриптор
-   [VtifulKernelExcel::header](vtiful-kernel-excel.header.md) - Записати заголовок
-   [VtifulKernelExcel::insertFormula](vtiful-kernel-excel.insertFormula.md) - Вставити формулу розрахунку
-   [VtifulKernelExcel::insertImage](vtiful-kernel-excel.insertImage.md) — Вставити зображення
-   [VtifulKernelExcel::insertText](vtiful-kernel-excel.insertText.md) — Вставити текст
-   [VtifulKernelExcel::mergeCells](vtiful-kernel-excel.mergeCells.md) - Об'єднати комірки
-   [VtifulKernelExcel::output](vtiful-kernel-excel.output.md) - Висновок
-   [VtifulKernelExcel::setColumn](vtiful-kernel-excel.setColumn.md) - Встановити стовпець
-   [VtifulKernelExcel::setRow](vtiful-kernel-excel.setRow.md) - Встановити рядок
