# TODOList

myself TODO list
# NASA World Wind
* https://support.google.com/webdesigner#topic=

#include "string.h"
int hextoten(char a[5])
{
int i,num;
 char ch;
 num=0;
 for(i=0;i<5;i++)
 {
ch=a[i];
 if((ch=='H')||(ch=='\0'))
   break;
 if ((ch>=0)&&(ch<='9'))
    ch=ch-'0';
 else
 ch=ch-'0'-7;
 num=num*16+ch;
 }
 return(num);
}

main()
{
char strhex[5]=“100”;
 int numten,k;
 strupr(strhex);
 numten=hextoten(strhex);
 printf("NUM=%d\n",numten);
}




