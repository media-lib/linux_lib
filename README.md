

* MAN pages: https://news.ycombinator.com/item?id=15775886
* C, Unix, and low-level programming: http://vendu.twodots.nl/wizardcode.html
* Comics: https://jvns.ca/teach-tech-with-cartoons/
* Command-line resources:
  * https://news.ycombinator.com/item?id=15507871
  * https://news.ycombinator.com/item?id=15514589
* Free C books: https://github.com/EbookFoundation/free-programming-books/blob/master/free-programming-books.md

* Regular expressions:
```bash
# === {{CMD}}  path/to/file
# === cat path/to/file | {{CMD}}  no-section
  html-no-section () {
    grep  -Pzo '(?s)(\A.+?)(?=\n\<!--)' $@
  }
# === {{CMD}}   STYLE|FOOT|...   path/to/file
# === cat path/to/file | {{CMD}}   STYLE|FOOT|...
  html-section () {
    section="$1"; shift
    grep  -Pzo '(?s)^\<!--\s+'$section'\s+-->\s?\n\K(.+?)(?=\n<!--|\Z)' $@
  }
```
