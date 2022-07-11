- [« Vtiful\Kernel\Excel::insertFormula](vtiful-kernel-excel.insertFormula.md)
- [Vtiful\Kernel\Excel::insertText »](vtiful-kernel-excel.insertText.md)

- [PHP Manual](index.md)
- [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)
- Вставити зображення

# Vtiful\Kernel\Excel::insertImage

(PECL xlswriter \>= 1.2.1)

Vtiful\Kernel\Excel::insertImage — Вставити зображення

### Опис

public **Vtiful\Kernel\Excel::insertImage**(int `$row`, int `$column`,
string `$localImagePath`)

Вставте локальне зображення в комірку.

### Список параметрів

`row`
рядок осередку

`column`
стовпець осередку

`localImagePath`
шлях до локального зображення

### Значення, що повертаються

Примірник [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

` <?php$config = [   'path' => './tests'];$excel = new \Vtiful\Kernel\Excel($config);$file = $excel->fileName("free.xlsx") ;$file->insertImage(5, 0, '/vagrant/ASW-G-66.jpg');$file->output(); `
