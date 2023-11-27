# WayBackTools

This utility is designed to work with the results from the Wayback Machine. It offers the following capabilities:
- Building a tree structure of the resource's directories and files.
- Generating a list of resource directories that can be utilized for file searches, for example, through dirsearch.

It is recommended to employ the utility on the output files of tools like [GAU](https://github.com/lc/gau#from-source), [Xurlfind3r](https://github.com/hueristiq/xurlfind3r) etc. 
However, you can also use it directly on the output of other tools. The key requirement is that the utility should only receive the URLs of the targets. There are plans to optimize this process in the future.

## Usage
```
$ gau "example.com" | waybtools -tr
$ cat "example.com" | waybtools -o TreeOutput.txt
$ cat "example.com" | waybtools -g DirsOutput.txt
$ xurlfind3r -d "example.com" | awk '{ print $2}' | waybtools -g DirsOutput.txt
```

