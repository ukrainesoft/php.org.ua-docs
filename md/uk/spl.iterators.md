Ітератори

-   [« SplObjectStorage::valid](splobjectstorage.valid.html)
    
-   [AppendIterator »](class.appenditerator.html)
    
-   [PHP Manual](index.html)
    
-   [SPL](book.spl.html)
    
-   Ітератори
    

# Ітератори

## Зміст

-   [AppendIterator](class.appenditerator.html)
-   [ArrayIterator](class.arrayiterator.html)
-   [CachingIterator](class.cachingiterator.html)
-   [CallbackFilterIterator](class.callbackfilteriterator.html)
-   [DirectoryIterator](class.directoryiterator.html)
-   [EmptyIterator](class.emptyiterator.html)
-   [FilesystemIterator](class.filesystemiterator.html)
-   [FilterIterator](class.filteriterator.html)
-   [GlobIterator](class.globiterator.html)
-   [InfiniteIterator](class.infiniteiterator.html)
-   [IteratorIterator](class.iteratoriterator.html)
-   [LimitIterator](class.limititerator.html)
-   [MultipleIterator](class.multipleiterator.html)
-   [NoRewindIterator](class.norewinditerator.html)
-   [ParentIterator](class.parentiterator.html)
-   [RecursiveArrayIterator](class.recursivearrayiterator.html)
-   [RecursiveCachingIterator](class.recursivecachingiterator.html)
-   [RecursiveCallbackFilterIterator](class.recursivecallbackfilteriterator.html)
-   [RecursiveDirectoryIterator](class.recursivedirectoryiterator.html)
-   [RecursiveFilterIterator](class.recursivefilteriterator.html)
-   [RecursiveIteratorIterator](class.recursiveiteratoriterator.html)
-   [RecursiveRegexIterator](class.recursiveregexiterator.html)
-   [RecursiveTreeIterator](class.recursivetreeiterator.html)
-   [RegexIterator](class.regexiterator.html)

SPL забезпечує набір ітераторів для обходу об'єктів.

## Дерево класів ітераторів SPL

-   [ArrayIterator](class.arrayiterator.html)
    -   [RecursiveArrayIterator](class.recursivearrayiterator.html)
-   [EmptyIterator](class.emptyiterator.html)
-   [IteratorIterator](class.iteratoriterator.html)
    -   [AppendIterator](class.appenditerator.html)
    -   [CachingIterator](class.cachingiterator.html)
        -   [RecursiveCachingIterator](class.recursivecachingiterator.html)
    -   [FilterIterator](class.filteriterator.html)
        -   [CallbackFilterIterator](class.callbackfilteriterator.html)
            -   [RecursiveCallbackFilterIterator](class.recursivecallbackfilteriterator.html)
        -   [RecursiveFilterIterator](class.recursivefilteriterator.html)
            -   [ParentIterator](class.parentiterator.html)
        -   [RegexIterator](class.regexiterator.html)
            -   [RecursiveRegexIterator](class.recursiveregexiterator.html)
    -   [InfiniteIterator](class.infiniteiterator.html)
    -   [LimitIterator](class.limititerator.html)
    -   [NoRewindIterator](class.norewinditerator.html)
-   [MultipleIterator](class.multipleiterator.html)
-   [RecursiveIteratorIterator](class.recursiveiteratoriterator.html)
    -   [RecursiveTreeIterator](class.recursivetreeiterator.html)
-   [DirectoryIterator](class.directoryiterator.html) (успадковує клас [SplFileInfo](class.splfileinfo.html)
    -   [FilesystemIterator](class.filesystemiterator.html)
        -   [GlobIterator](class.globiterator.html)
        -   [RecursiveDirectoryIterator](class.recursivedirectoryiterator.html)