```sh
$ command | grep <search_string>

$ command | grep -v <search_string> # excludes search_string

$ grep <search_string> file #also searchs the word
```
## Option flags
```sh
-n # shows line number

-c # count of search_string but doesn'nt print line

-i # case insensitive search

-v # excludes the search_string
```
>**By default grep is case-sensetive**

```sh
$ grep <search_string> * #also searchs the word in all files in the dir

$ grep -r <search_string> dir # recurrsive search

$ grep -r <search_string> /path/to/folder

$ grep <search_string> /path/to/file 
```