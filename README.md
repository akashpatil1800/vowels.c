# vowels.c
Child process calculates total no of vowels

 
#include<stdio.h>
 
#include<stdlib.h>
 
#include<unistd.h>
 
int main()
 
{
 
char line[150];
 
int i,vowels,ptd;
 
printf( " enter the words so child process counts the number of vowel words \n");
 
fgets(line,sizeof(line),stdin);
 
ptd = fork();
 
if (ptd ==0)
 
{
 
printf("child process counting");
 
for ( i=0; line[i] != '\0'; ++i)
 
{
 
 
if(line[i] =='a' || line[i] == 'e' || line[i] =='i' ||
 
   line[i] =='o' || line[i] == 'u' || line[i] =='A' ||
 
   line[i] =='E' || line[i] == 'I' || line[i] =='O' ||
 
   line[i] =='U') {
 
   ++vowels;
 
   }
 
   }
 
   printf("Vowels: %d",vowels);
 
   return 0;
 
   }
 
   }
