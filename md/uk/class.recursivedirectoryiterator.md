- [« RecursiveCallbackFilterIterator::hasChildren](recursivecallbackfilteriterator.haschildren.md)
- [RecursiveDirectoryIterator::\_\_construct »](recursivedirectoryiterator.construct.md)

- [PHP Manual](index.md)
- [Ітератори](spl.iterators.md)
- Клас RecursiveDirectoryIterator

# Клас RecursiveDirectoryIterator

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас **RecursiveDirectoryIterator** надає інтерфейс для
рекурсивного перебору каталогів файлової системи

## Огляд класів

class **RecursiveDirectoryIterator** extends
[FilesystemIterator](class.filesystemiterator.md) implements
[RecursiveIterator](class.recursiveiterator.md) {

/\* Успадковані константи \*/

const int `FilesystemIterator::CURRENT_AS_PATHNAME` = 32;

const int `FilesystemIterator::CURRENT_AS_FILEINFO` = 0;

const int `FilesystemIterator::CURRENT_AS_SELF` = 16;

const int `FilesystemIterator::CURRENT_MODE_MASK` = 240;

const int `FilesystemIterator::KEY_AS_PATHNAME` = 0;

const int `FilesystemIterator::KEY_AS_FILENAME` = 256;

const int `FilesystemIterator::FOLLOW_SYMLINKS` = 512;

const int `FilesystemIterator::KEY_MODE_MASK` = 3840;

const int `FilesystemIterator::NEW_CURRENT_AND_KEY` = 256;

const int `FilesystemIterator::SKIP_DOTS` = 4096;

const int `FilesystemIterator::UNIX_PATHS` = 8192;

/\* Методи \*/

public [\_\_construct](recursivedirectoryiterator.construct.md)(string
`$directory`, int `$flags` = FilesystemIterator::KEY_AS_PATHNAME \|
FilesystemIterator::CURRENT_AS_FILEINFO)

public [getChildren](recursivedirectoryiterator.getchildren.md)():
[RecursiveDirectoryIterator](class.recursivedirectoryiterator.md)

public [getSubPath](recursivedirectoryiterator.getsubpath.md)():
string

public
[getSubPathname](recursivedirectoryiterator.getsubpathname.md)():
string

public [hasChildren](recursivedirectoryiterator.haschildren.md)(bool
`$allowLinks` = **`false`**): bool

public [key](recursivedirectoryiterator.key.md)(): string

public [next](recursivedirectoryiterator.next.md)(): void

public [rewind](recursivedirectoryiterator.rewind.md)(): void

/\* Наслідувані методи \*/

public [FilesystemIterator::current](filesystemiterator.current.md)():
string\|[SplFileInfo](class.splfileinfo.md)\|[FilesystemIterator](class.filesystemiterator.md)

public
[FilesystemIterator::getFlags](filesystemiterator.getflags.md)(): int

public [FilesystemIterator::key](filesystemiterator.key.md)(): string

public [FilesystemIterator::next](filesystemiterator.next.md)(): void

public [FilesystemIterator::rewind](filesystemiterator.rewind.md)():
void

public
[FilesystemIterator::setFlags](filesystemiterator.setflags.md)(int
`$flags`): void

public [DirectoryIterator::current](directoryiterator.current.md)():
[mixed](language.types.declarations.md#language.types.declarations.mixed)

public [DirectoryIterator::getATime](directoryiterator.getatime.md)():
int

public
[DirectoryIterator::getBasename](directoryiterator.getbasename.md)(string
`$suffix` = ""): string

public [DirectoryIterator::getCTime](directoryiterator.getctime.md)():
int

public
[DirectoryIterator::getExtension](directoryiterator.getextension.md)():
string

public
[DirectoryIterator::getFilename](directoryiterator.getfilename.md)():
string

public [DirectoryIterator::getGroup](directoryiterator.getgroup.md)():
int

public [DirectoryIterator::getInode](directoryiterator.getinode.md)():
int

public [DirectoryIterator::getMTime](directoryiterator.getmtime.md)():
int

public [DirectoryIterator::getOwner](directoryiterator.getowner.md)():
int

public [DirectoryIterator::getPath](directoryiterator.getpath.md)():
string

public
[DirectoryIterator::getPathname](directoryiterator.getpathname.md)():
string

public [DirectoryIterator::getPerms](directoryiterator.getperms.md)():
int

public [DirectoryIterator::getSize](directoryiterator.getsize.md)():
int

public [DirectoryIterator::getType](directoryiterator.gettype.md)():
string

public [DirectoryIterator::isDir](directoryiterator.isdir.md)(): bool

public [DirectoryIterator::isDot](directoryiterator.isdot.md)(): bool

public
[DirectoryIterator::isExecutable](directoryiterator.isexecutable.md)():
bool

public [DirectoryIterator::isFile](directoryiterator.isfile.md)():
bool

public [DirectoryIterator::isLink](directoryiterator.islink.md)():
bool

public
[DirectoryIterator::isReadable](directoryiterator.isreadable.md)():
bool

public
[DirectoryIterator::isWritable](directoryiterator.iswritable.md)():
bool

public [DirectoryIterator::key](directoryiterator.key.md)():
[mixed](language.types.declarations.md#language.types.declarations.mixed)

public [DirectoryIterator::next](directoryiterator.next.md)(): void

public [DirectoryIterator::rewind](directoryiterator.rewind.md)():
void

public [DirectoryIterator::seek](directoryiterator.seek.md)(int
`$offset`): void

public
[DirectoryIterator::\_\_toString](directoryiterator.tostring.md)():
string

public [DirectoryIterator::valid](directoryiterator.valid.md)(): bool

public [SplFileInfo::getATime](splfileinfo.getatime.md)(): int\|false

public [SplFileInfo::getBasename](splfileinfo.getbasename.md)(string
`$suffix` = ""): string

public [SplFileInfo::getCTime](splfileinfo.getctime.md)(): int\|false

public [SplFileInfo::getExtension](splfileinfo.getextension.md)():
string

public [SplFileInfo::getFileInfo](splfileinfo.getfileinfo.md)(?string
`$class` = **`null`**): [SplFileInfo](class.splfileinfo.md)

public [SplFileInfo::getFilename](splfileinfo.getfilename.md)():
string

public [SplFileInfo::getGroup](splfileinfo.getgroup.md)(): int\|false

public [SplFileInfo::getInode](splfileinfo.getinode.md)(): int\|false

public [SplFileInfo::getLinkTarget](splfileinfo.getlinktarget.md)():
string\|false

public [SplFileInfo::getMTime](splfileinfo.getmtime.md)(): int\|false

public [SplFileInfo::getOwner](splfileinfo.getowner.md)(): int\|false

public [SplFileInfo::getPath](splfileinfo.getpath.md)(): string

public [SplFileInfo::getPathInfo](splfileinfo.getpathinfo.md)(?string
`$class` = **`null`**): ?[SplFileInfo](class.splfileinfo.md)

public [SplFileInfo::getPathname](splfileinfo.getpathname.md)():
string

public [SplFileInfo::getPerms](splfileinfo.getperms.md)(): int\|false

public [SplFileInfo::getRealPath](splfileinfo.getrealpath.md)():
string\|false

public [SplFileInfo::getSize](splfileinfo.getsize.md)(): int\|false

public [SplFileInfo::getType](splfileinfo.gettype.md)(): string\|false

public [SplFileInfo::isDir](splfileinfo.isdir.md)(): bool

public [SplFileInfo::isExecutable](splfileinfo.isexecutable.md)():
bool

public [SplFileInfo::isFile](splfileinfo.isfile.md)(): bool

public [SplFileInfo::isLink](splfileinfo.islink.md)(): bool

public [SplFileInfo::isReadable](splfileinfo.isreadable.md)(): bool

public [SplFileInfo::isWritable](splfileinfo.iswritable.md)(): bool

public [SplFileInfo::openFile](splfileinfo.openfile.md)(string `$mode`
= "r", bool `$useIncludePath` = **`false`**, ?resource `$context` =
**`null`**): [SplFileObject](class.splfileobject.md)

public [SplFileInfo::setFileClass](splfileinfo.setfileclass.md)(string
`$class` = SplFileObject::class): void

public [SplFileInfo::setInfoClass](splfileinfo.setinfoclass.md)(string
`$class` = SplFileInfo::class): void

public [SplFileInfo::\_\_toString](splfileinfo.tostring.md)(): string

}

## Зміст

- [RecursiveDirectoryIterator::\_\_construct](recursivedirectoryiterator.construct.md)
- Конструктор класу RecursiveDirectoryIterator
- [RecursiveDirectoryIterator::getChildren](recursivedirectoryiterator.getchildren.md)
— Якщо поточний елемент є директорією, метод повертає
її ітератор
- [RecursiveDirectoryIterator::getSubPath](recursivedirectoryiterator.getsubpath.md)
— Повертає шлях до піддиректорії
- [RecursiveDirectoryIterator::getSubPathname](recursivedirectoryiterator.getsubpathname.md)
— Повертає шлях до піддиректорії та ім'я файлу
- [RecursiveDirectoryIterator::hasChildren](recursivedirectoryiterator.haschildren.md)
— Визначає, чи поточний елемент є директорією
- [RecursiveDirectoryIterator::key](recursivedirectoryiterator.key.md)
— Повертає шлях та ім'я файлу поточного елемента
- [RecursiveDirectoryIterator::next](recursivedirectoryiterator.next.md)
— Перехід до наступного елементу
- [RecursiveDirectoryIterator::rewind](recursivedirectoryiterator.rewind.md)
— перекладає ітератор на початок директорії
