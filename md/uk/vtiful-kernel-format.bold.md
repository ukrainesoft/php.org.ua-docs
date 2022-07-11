- [« Vtiful\Kernel\Format::align](vtiful-kernel-format.align.md)
- [Vtiful\Kernel\Format::italic »](vtiful-kernel-format.italic.md)

- [PHP Manual](index.md)
- [Vtiful\Kernel\Format](class.vtiful-kernel-format.md)
- Напівжирний

# Vtiful\Kernel\Format::bold

(PECL xlswriter \>= 1.2.1)

Vtiful\Kernel\Format::bold - Напівжирний

### Опис

public **Vtiful\Kernel\Format::bold**(resource `$handle`)

Напівжирний формат
[Vtiful\Kernel\Format](class.vtiful-kernel-format.md)

### Список параметрів

`handle`
Дескриптор файлу xlsx

### Значення, що повертаються

Ресурс

### Приклади

**Приклад #1 Приклад використання**

` <?php$config = [   'path' => './tests'];$excel  = new \Vtiful\Kernel\Excel($config);$fileObject = $excel->fileName('tutorial01.xlsx') ;$fileHandle==$fileObject->getHandle();$boldStyle==\Vtiful\Kernel\Format::bold($fileHandle);$fileObject->header(['name', 'age'])    ->data([ ['viest', 21]])   ->setColumn('A:A', 200, $boldStyle)   ->output();?> `
