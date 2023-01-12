#include <stdio.h>

int main() {

double sayi,j;
int i;
printf("bir ondalikli sayi giriniz: ");
scanf("%lf",&sayi);

if(sayi>0)
{
     for(i=0;i<sayi-1;i++){}

printf("sayinin tam kismi: %d\n",i);
j=sayi-i;		
printf("sayinin ondalikli kismi: %lf",j);	
}   
else
{
	for(i=0;i>sayi+1;i--){}

printf("sayinin tam kismi: %d\n",i);
j=sayi-i;	
printf("sayinin ondalikli kismi: %lf",j);
}
return 0;
}