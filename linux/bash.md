## Основные команды
```bash
# справка
help
# история
history
# очистка
clear
# выход
exit
```
## Создание директории
```bash
# создание директории
mkdir [dirname]
# несколько диреторий
mkdir -p {dir1,dir2}
# несколько вложенных директорий
mkdir -p my-app/{css,js}
```
## Список файлов
```bash
# лист
ls
# включая скрытые файлы
ls -a | -f
# больше информации
# например права доступа
ls -l
```
## Создание файла
```bash
touch [file-name]
# несколько файлов
touch my-app/{index.html,css/style.css,js/script.js}
```
## Содержимое файла
```bash
cat [file-name]
# меньше контента
less [file-name] // q - exit
```
## Движение файла
```bash
# copy
cp [file1] [file2]
# move
mv [file1] [file2]
# пример перемещения всех файлов
# из одной директории в другую
mv [dir1]/*.* [dir2]
# удаление
rm [file-name]
# удаление пустой директории
rmdir [dir-name]
# удаление непустой директории
rm -r [dir-name]
# или
rm -rf [dir-name]
```
## Загрузка файла
```bash
wget [url]
```
