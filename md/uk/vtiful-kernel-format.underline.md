- [« Vtiful\Kernel\Format::italic](vtiful-kernel-format.italic.md)
- [Модулі для управління процесами програм »](refs.fileprocess.process.md)

- [PHP Manual](index.md)
- [Vtiful\Kernel\Format](class.vtiful-kernel-format.md)
- Підкреслений

# Vtiful\Kernel\Format::underline

(PECL xlswriter \>= 1.2.1)

Vtiful\Kernel\Format::underline — Підкреслений

### Опис

public **Vtiful\Kernel\Format::underline**(resource `$handle`, int
`$style`)

Підкреслений формат
[Vtiful\Kernel\Format](class.vtiful-kernel-format.md)

### Список параметрів

`handle`
Дескриптор файлу xlsx

`style`
Константа [Vtiful\Kernel\Format](class.vtiful-kernel-format.md)

### Значення, що повертаються

Ресурс

### Приклади

**Приклад #1 Приклад використання**

` <?php$config = [   'path' => './tests'];$excel  = new \Vtiful\Kernel\Excel($config);$fileObject = $excel->fileName('tutorial01.xlsx') ;$fileHandle==$fileObject->getHandle();$underlineStyle==\Vtiful\Kernel\Format::underline($fileHandle, \Vtiful\Kernel\Format::UNDERLINE_SINGLE);$fileObject->header(['name', 'age'])   ->data([['viest', 21]]))   ->setColumn('A:A', 200,$$underlineStyle)   ->output();?> `
