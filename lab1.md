```
[user@sahara ~/lecture1]$ cd
[user@sahara ~]$ 
```
> Directory was ˜/lecture1
> Output was just the changed directory, whenever you use cd command with no arguments you just go to root.
> The output is not an error

```
[user@sahara ~]$ ls
lecture1
```
> Directory was root
> Output was the items in the root directory
> Output is not an error
  

```
[user@sahara ~]$ cat

```
> Directory was root
> Nothing showed up, it was waiting for an input when no arguments are given
> Output is not an error
  

```
[user@sahara ~]$ cd lecture1/
[user@sahara ~/lecture1]$
```
> Directory was root
> Navigated to lecture1 directory, no other output
> Output is not an error
  

```
[user@sahara ~/lecture1]$ ls messages
en-us.txt  es-mx.txt  pt-br.txt  zh-cn.txt
```
> Directory was lecture1
> Output was the list of items in messages directory
> Output is not an error
  

```
[user@sahara ~/lecture1]$ cat messages
cat: messages: Is a directory
```
> Directory was lecture1
> Output is an error message explaining that you can't use cat with a directory
> Message is an error, cat is not allowed with a directory
  

```
[user@sahara ~/lecture1]$ cd Hello.java
bash: cd: Hello.java: Not a directory
```
> Directory was lecture1
> Output is an error message stating file is not a directory
> Output is an error, can't navigate to file
   

```
[user@sahara ~/lecture1]$ ls Hello.java
Hello.java
```
> Directory was lecture1
> Output was the file name passed in the argument, ls lists the items in the arguments passed, if it is a file it just prints file name
> Not an error
   

```
[user@sahara ~/lecture1]$ cat Hello.java
import java.io.IOException;
import java.nio.charset.StandardCharsets;
import java.nio.file.Files;
import java.nio.file.Path;

public class Hello {
  public static void main(String[] args) throws IOException {
    String content = Files.readString(Path.of(args[0]), StandardCharsets.UT
F_8);    
    System.out.println(content);
  }
}
```
> Directory was lecture1
> Output was the contents of the Hello.java file
> Output was not an error
