# WayBackTools

This utility is designed to work with the results from the Wayback Machine. It offers the following capabilities:
- Building a tree structure of the resource's directories and files.
- Generating a list of resource directories that can be utilized for file searches, for example, through dirsearch.

It is recommended to employ the utility on the output files of tools like [GAU](https://github.com/lc/gau#from-source), [Xurlfind3r](https://github.com/hueristiq/xurlfind3r) etc. 
However, you can also use it directly on the output of other tools. The key requirement is that the utility should only receive the URLs of the targets. There are plans to optimize this process in the future.

## Installation

```
$ git clone https://github.com/n3170n/WayBackTools.git
$ sudo cp waybtools /usr/local/bin/waybtools
```

## Usage
```
$ gau -u "example.com" | waybtools -tr
$ cat "example.com" | waybtools -o TreeOutput.txt
$ cat "example.com" | waybtools -g DirsOutput.txt
$ xurlfind3r -d "example.com" | awk '{ print $2}' | waybtools -g DirsOutput.txt
```
To display the help for the tool use the -h flag:
```
waybtools -h
```

|Flag|Description|Example| 
|----|----|----|
| -g  | Generate  directory list | waybtools -g dirs.txt    |
| -o  | Save the generated tree to a file | waybtools -o file.txt |
| -tr | Display the resource tree | waybtools -tr               |
| -l  | Extract links with parameters | waybtools -l links.txt | 
