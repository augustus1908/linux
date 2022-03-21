# Search text files

## 1. Search for text with `grep` - global regular expression print
grep [option] pattern [file]

* `-c` : This prints only a count of the lines that match a pattern

* `-h` : Display the matched lines, but do not display the filenames.

* `-i` : Ignores, case for matching

* `-l` : Displays list of a filenames only.

* `-n` : Display the matched lines and their line numbers.

* `-v` : This prints out all the lines that do not matches the pattern

* `-e exp` : Specifies expression with this option. Can use multiple times.
* `-f file` : Takes patterns from file, one per line.

* `-E` : Treats pattern as an extended regular expression (ERE)
* `-w` : Match whole word

* `-o` : Print only the matched parts of a matching line,
 with each such part on a separate output line.

* `-A n` : Prints searched line and nlines after the result.

* `-B n` : Prints searched line and n line before the result.

* `-C n` : Prints searched line and n lines after before the result.




## 2. sed - stream editor
sed [option] [script] [file]
![](https://f7-zpcloud.zdn.vn/7586727154783301945/1ed8d4628b9844c61d89.jpg)

tìm kiếm, tìm và thay thế, chèn hoặc xóa

![](https://f5-zpcloud.zdn.vn/3956542292709535265/4db0a6f5f10f3e51671e.jpg)
![](https://f6-zpcloud.zdn.vn/7112369155395736290/1160b994ee6e2130787f.jpg)





























