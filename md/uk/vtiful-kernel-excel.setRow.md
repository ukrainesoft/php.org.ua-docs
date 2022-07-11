- [« Vtiful\Kernel\Excel::setColumn](vtiful-kernel-excel.setColumn.md)
- [Vtiful\Kernel\Format »](class.vtiful-kernel-format.md)

- [PHP Manual](index.md)
- [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)
- Встановити рядок

# Vtiful\Kernel\Excel::setRow

(PECL xlswriter \>= 1.2.1)

Vtiful\Kernel\Excel::setRow — Встановити рядок

### Опис

public **Vtiful\Kernel\Excel::setRow**(string `$range`, float `$height`,
resource `$format` = ?)

Встановити формат рядка.

### Список параметрів

`range`
початкові та кінцеві рядки координат осередку

`height`
висота рядка

`format`
ресурс формату осередку

### Значення, що повертаються

Примірник [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

` <?php$config = [   'path' => './tests'];$excel  = new \Vtiful\Kernel\Excel($config);$fileObject = $excel->fileName('tutorial01.xlsx') ;$fileHandle==$fileObject->getHandle();$boldStyle = \Vtiful\Kernel\Format::bold($fileHandle);$fileObject->header(['name', 'age'])    ->data([ ['viest', 21]])   ->setRow('A1', 20, $boldStyle,)   ->output(); `
