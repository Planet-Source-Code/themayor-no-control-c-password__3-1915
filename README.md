<div align="center">

## No Control C Password


</div>

### Description

This is a password script. Every charachter the user input it displays a star. the password is

kcTHEgreat. Catches Control c (Taught to me by a friend :)) so the only way out is to enter the correct password. If you like and think it's secure put it in your autoexec.bat
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[theMayor](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/themayor.md)
**Level**          |Beginner
**User Rating**    |4.8 (19 globes from 4 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Security](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/security__3-14.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/themayor-no-control-c-password__3-1915/archive/master.zip)





### Source Code

```
#include <iostream.h>
#include <conio.h>
#include <stdlib.h>
#include <signal.h>
#include <string>
#include <dos.h>
void restart();
void loop(int signal)
{
 return;
}
int main()
{
 system ("cls");
 char key;
 char password[] ="kcTHEgreat";// your password goes here
 int counter=0;
 char kcpassword[counter];
 cout << "Password: ";
 cout << flush;
 for (;;)
 {
 if (signal(SIGINT, loop)) {};
 cout << flush;
 key=getch();
 if (key=='\r')
 {
 break;
 }
 else
 {
 cout << flush;
 kcpassword[counter]=key;
 counter++;
 cout << "*";
 }
 }
 int flag=1;
 for (int x=0;x<counter;x++)
 {
 if (kcpassword[x]!=password[x] || strlen(password)!=counter)
 {
 flag=0;
 break;
 }
 }
 system ("cls");
 if (counter==0)
 restart();
 if (flag==0)
 {
 gotoxy(35,10);textcolor(12);cprintf("!!DENIED!!");
 delay(1000);
 restart();
 }
 else
 {
 gotoxy(30,10);textcolor(12);cprintf("!!ACCESS GRANTED!!");
 for (int x=0;x<3000;x++);
 delay(1000);
 }
 return 0;
}
void restart()
{
 main();
}
```

