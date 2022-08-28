Клас Directory

-   [« Предопределённые константы](dir.constants.html)
    
-   [Directory::close »](directory.close.html)
    
-   [PHP Manual](index.html)
    
-   [Каталоги](book.dir.html)
    
-   Клас Directory
    

# Клас Directory

(PHP 4, PHP 5, PHP 7, PHP 8)

## Вступ

Примірники класу **Directory** створюються за допомогою виклику функції [dir()](function.dir.html), а не за допомогою оператора [new](language.oop5.basic.html#language.oop5.basic.new)

## Огляд класів

```classsynopsis

     
    

    
     
      class Directory
     
     {

    /* Свойства */
    
     public
     readonly
     string
      $path;

    public
     readonly
     resource
      $handle;


    /* Методы */
    
   public close(): void
public read(): string|false
public rewind(): void

   }
```

## Властивості

path

Каталог, який було відкрито.

handle

Може використовуватися з іншими функціями каталогів, такими як [readdir()](function.readdir.html) [rewinddir()](function.rewinddir.html) і [closedir()](function.closedir.html)

## список змін

| Версия | Описание                                                    |
|--------|-------------------------------------------------------------|
|        | Властивості path та handle тепер доступні лише для читання. |

## Зміст

-   [Directory::close](directory.close.html) — Закриває дескриптор каталогу
-   [Directory::read](directory.read.html) — Отримує елемент із дескриптора каталогу
-   [Directory::rewind](directory.rewind.html) — Переміщує дескриптор каталогу на початок каталогу