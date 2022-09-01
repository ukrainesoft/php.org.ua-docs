---
navigation:
  - xlswriter.constants.md: « Обумовлені константи
  - vtiful-kernel-excel.addSheet.html: 'VtifulKernelExcel::addSheet »'
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
public insertText(    int $row,    int $column,    stringintdouble $data,    string $format = ?)
public mergeCells(string $scope, string $data)
public output()
public setColumn(string $range, float $width, resource $format = ?)
public setRow(string $range, float $height, resource $format = ?)


   }
```

## Зміст

-   [VtifulKernelExcel::addSheet](vtiful-kernel-excel.addSheet.html) - Додати лист
-   [VtifulKernelExcel::autoFilter](vtiful-kernel-excel.autoFilter.html) - Додати автофільтр
-   [VtifulKernelExcel::constMemory](vtiful-kernel-excel.constMemory.html) - Кількість пам'яті
-   [VtifulKernelExcel::construct](vtiful-kernel-excel.construct.html) - Конструктор
-   [VtifulKernelExcel::data](vtiful-kernel-excel.data.html) - Записати дані
-   [VtifulKernelExcel::fileName](vtiful-kernel-excel.filename.html) — Створити назву файлу
-   [VtifulKernelExcel::getHandle](vtiful-kernel-excel.getHandle.html) - Отримати дескриптор
-   [VtifulKernelExcel::header](vtiful-kernel-excel.header.html) - Записати заголовок
-   [VtifulKernelExcel::insertFormula](vtiful-kernel-excel.insertFormula.html) - Вставити формулу розрахунку
-   [VtifulKernelExcel::insertImage](vtiful-kernel-excel.insertImage.html) — Вставити зображення
-   [VtifulKernelExcel::insertText](vtiful-kernel-excel.insertText.html) — Вставити текст
-   [VtifulKernelExcel::mergeCells](vtiful-kernel-excel.mergeCells.html) - Об'єднати комірки
-   [VtifulKernelExcel::output](vtiful-kernel-excel.output.html) - Висновок
-   [VtifulKernelExcel::setColumn](vtiful-kernel-excel.setColumn.html) - Встановити стовпець
-   [VtifulKernelExcel::setRow](vtiful-kernel-excel.setRow.html) - Встановити рядок
