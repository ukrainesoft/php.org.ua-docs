- [« Vtiful\Kernel\Excel::insertImage](vtiful-kernel-excel.insertImage.md)
- [Vtiful\Kernel\Excel::mergeCells »](vtiful-kernel-excel.mergeCells.md)

- [PHP Manual](index.md)
- [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)
- Вставити текст

# Vtiful\Kernel\Excel::insertText

(PECL xlswriter \>= 1.2.1)

Vtiful\Kernel\Excel::insertText — Вставити текст

### Опис

public **Vtiful\Kernel\Excel::insertText**(
int `$row`,
int `$column`,
stringintdouble `$data`,
string `$format` = ?
)

Вставити текст у комірку.

### Список параметрів

`row`
рядок осередку

`column`
стовпець осередку

`data`
дані для запису

`format`
формат рядка

### Значення, що повертаються

Примірник [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

` <?php$config = [   'path' => './tests'];$excel = new \Vtiful\Kernel\Excel($config);$file = $excel->fileName("free.xlsx") ->header(['name', 'money']);for ($index = 0; $index < 10; $index++) {   $file->insertText($index+1, 0, 'viest'); $file->insertText($index+1, 1, 10000, '#,##0');}$textFile->output(); `
