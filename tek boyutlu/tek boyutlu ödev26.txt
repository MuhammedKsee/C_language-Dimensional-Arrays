#include <stdio.h>

int main() {

int n,i,enbuyuk=1,enkucuk=1;
printf("basamak sayisi giriniz: ");
scanf("%d",&n);
for(i=1;i<=n;i++)
{
	enbuyuk*=10;
}
enkucuk=enbuyuk/10;
enbuyuk--;
printf("%d",enbuyuk-enkucuk);
return 0;
}