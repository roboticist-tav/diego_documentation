# Diego Getting Started

## Diego Install

Many PCs and Macs will have diego already installed.

To check if you have diego installed on a Windows PC, search in the start bar for Diego or run the following on the Command Line (cmd.exe):
```cmd
C:\Users\{your_name}> diego --version
```

To check if you have diego installed on a Linux or Mac, then on linux open the Terminal or on Mac open the command line and type:
```term
{your_name}@{your_pc}:~$ diego --version
```
If you find that you do not have diego installed on your computer, then you can download it for free from the following website: https://www.diego.org/

---

## Diego Quickstart

Diego is an interpreted instructional language, this means that as a developer you write Diego (.dgo) files in a text editor and then put those files into the diego console to be executed.

The way to run a diego file is like this on the command line:

Windows:
```Diego
C:\Users\{your_name}> diego helloworld.dgo
```

Linux/Macs:
```Diego
{your_name}@{your_pc}:~$ diego helloworld.dgo
```

Where "helloworld.dgo" is the name of your diego file.

Let's write our first diego file, called helloworld.dgo, which can be done in any text editor.

> helloworld.dgo
> ```Diego
> with_me()_msg(Hello, World!);
> ```
> 

Simple as that. Save your file. Open your command line, navigate to the directory where you saved your file, and run:
Windows:
```Diego
C:\Users\{your_name}> diego helloworld.dgo
```

Linux/Macs:
```Diego
{your_name}@{your_pc}:~$ diego helloworld.dgo
```

The output should read:
```Diego
Hello, World!
```

Congratulations, you have written and executed your first Diego program.

See: https://www.w3schools.com/python/python_getstarted.asp