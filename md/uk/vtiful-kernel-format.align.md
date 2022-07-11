- [« Vtiful\Kernel\Format](class.vtiful-kernel-format.md)
- [Vtiful\Kernel\Format::bold »](vtiful-kernel-format.bold.md)

- [PHP Manual](index.md)
- [Vtiful\Kernel\Format](class.vtiful-kernel-format.md)
- Вирівнювання

# Vtiful\Kernel\Format::align

(PECL xlswriter \>= 1.2.1)

Vtiful\Kernel\Format::align — Вирівнювання

### Опис

public **Vtiful\Kernel\Format::align**(resource `$handle`, int `$style`)

Встановити вирівнювання осередку

### Список параметрів

`handle`
Дескриптор файлу xlsx

`style`
Константа [Vtiful\Kernel\Format](class.vtiful-kernel-format.md)

### Значення, що повертаються

Ресурс

### Приклади

**Приклад #1 Приклад використання**

` <?php$config = [   'path' => './tests'];$excel  = new \Vtiful\Kernel\Excel($config);$fileObject = $excel->fileName('tutorial01.xlsx') ;$fileHandle==$fileObject->getHandle();$alignStyle==\Vtiful\Kernel\Format::align($fileHandle, \Vtiful\Kernel\Format::FORMAT_ALIGN_LEFT);$fileObject->header(['name', 'age'])   ->data([['viest', 21]]))    ->setColumn('A:A', 200, $align)   ->output();?> `
