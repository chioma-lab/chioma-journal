# File Types

As we wander around our Linux system, it is helpful to determine what kind of data a file contains before we try to view it. This is where the file command comes in. file will examine a file and tell us what kind of file it is.

To use the file program, we just type:

```
file name_of_file
```

The file program can recognize most types of files, such as:


## Various kinds of files

|File Type|Description|Viewable as text?|
|:---|:---|:---|
|ASCII text|The name says it all|yes|
|Bourne-Again shell script text|A bash script|yes|
|ELF 64-bit LSB executable|An executable binary program|no|
|ELF 64-bit LSB shared object|A shared library|no|
|GNU tar archive|A tape archive file. A common way of storing groups of files.|no, use tar tvf to view listing.|
|gzip compressed data|An archive compressed with gzip|no|
|HTML document text|A web page|yes|
|JPEG image data|A compressed JPEG image|no|
|PostScript document text|A PostScript file|yes|
|Zip archive data|An archive compressed with zip|no|
