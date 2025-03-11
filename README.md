# 📝 Text2TableX
A project developed for personal purposes because I was tired of spending more time making tables for school projects than getting information!

Text2TableX offers the possibility of transforming plain text with format to a Docx table in a simple way. 
To run the program you simply need to call it and pass it two arguments: 

+ The first is the path (--path), the path where the file to be interpreted and transformed into .docx tables is located.
+ The second is the output (--output), the name and path that the file will have after being created (this is optional, by default it is "output.docx").

Example: 
```
python.exe Text2TableX.py --path example.txt --output output.docx
```

# 📁 Interpretable files

Interpretable files must have a specific text format, which can be seen in the file "[example.txt](https://github.com/Kr3my/Text2TableX/blob/main/example.txt)".

The format has three keywords, which are "header", "content" and "endtable":

+ **Header:** Creates a header and contains the text of the header, it must be created at the beginning of the current table.
+ **Content:** Create new content in the table in order, if there are 3 headers then 3 content will have to be made to fill an entire row.
+ **Endtable:** Ends the current table and allows new ones to be created below (it must be placed at the end of each table to mark its end)

Keywords are not case sensitive, note that they only create new rows, as columns are automatically created once the content has filled all the headers.

## Example seen in example.txt file:

Interpretable file:
```
header: Header 1
header: Header 2

content: Content 1
content: Content 2

endtable

header: Header 1
header: Header 2
header: Header 3

content: Content 1
content: Content 2
content: Content 3

content: Content 4
content: Content 5
content: Content 6

endtable
```

Command:
```
python.exe Text2TableX.py --path example.txt
```

Output:

![image](https://github.com/user-attachments/assets/255cef37-331f-49c7-b422-3f79e1c1b612)

This program simply generates a very basic table, but it can be configured manually as it is a .docx file. In my case, this saves me a lot of work when doing schoolwork since I'm pretty bad at using these files.
