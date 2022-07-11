- [« Vtiful\Kernel\Excel::output](vtiful-kernel-excel.output.md)
- [Vtiful\Kernel\Excel::setRow »](vtiful-kernel-excel.setRow.md)

- [PHP Manual](index.md)
- [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)
- встановити стовпець

# Vtiful\Kernel\Excel::setColumn

(PECL xlswriter \>= 1.2.1)

Vtiful\Kernel\Excel::setColumn — Встановити стовпець

### Опис

public **Vtiful\Kernel\Excel::setColumn**(string `$range`, float
`$width`, resource `$format` = ?)

Встановити формат шпальти.

### Список параметрів

`range`
початкові та кінцеві рядки координат осередку

`width`
ширина стовпця

`format`
ресурс формату осередку

### Значення, що повертаються

Примірник [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

` <?php$config = [   'path' => './tests'];$excel  = new \Vtiful\Kernel\Excel($config);$fileObject = $excel->fileName('tutorial01.xlsx') ;$fileHandle==$fileObject->getHandle();$boldStyle = \Vtiful\Kernel\Format::bold($fileHandle);$fileObject->header(['name', 'age'])    ->data([ ['viest', 21]])   ->setColumn('A:A', 200, $boldStyle)   ->output(); `
