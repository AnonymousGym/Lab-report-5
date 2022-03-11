# __Lab Report 4__

First, I ran the bash script with both Joe's version of MarkdownParse and my own MarkdownParse using the following command:

```
time bash script.sh>results.txt
```
and
```
time bash script.sh>resultsOld.txt
```

Now I have two results.txt. I use the command to compare two results.txt:

```
diff results.txt resultsOld.txt
```
# First Example

Here we can see the link in 22.md is valid.
![Image][11]

[11]: 1.png

Here are the two results.
![Image][12]

[12]: 2.png
![Image][13]

[13]: 3.png

Apparently, my code is correct but Joe's is not. The two versions of code are listed.

![Image][17]

[17]: 7.png

![Image][18]

[18]: 8.png

The reason for this is that in Joe's MarkdownParse, it checks the index of "". It returns the link only if the index of "" is -1. In other words, it returns the output only if there is no "" in the link. Therefore, the following part of code should be fixed to deal with the conditions that the links are valid with "".

# Second Example
