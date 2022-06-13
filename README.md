# parser

1. Попытка найти дублирующиеся адреса в файле, используя принцип работы HashMap и парсер SAX.
Итог - OutOfMemoryException и переполнение кучи, так как файл слишком большой. На файле меньше размером работает и находит дубликаты.

2. Выбран другой способ - разбиение на несколько файлов, сортировка строк внутри этих файлов и последующая сортировка файлов слиянием. 
Таким образом, файл не будет полностью выгружаться в память.
Пришлось увеличить размер кучи до ~1700 MiB. 
