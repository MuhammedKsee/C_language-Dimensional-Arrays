#include <stdio.h>
#include <stdlib.h>



int main() {
	
	int n,A[10],B[10],C[10],i,ort,toplam=0,a,b;
	
	printf("diziniz kac elemanli olsunn");
	scanf("%d",&n);
	
	for (i=0;i<n;i++)
	{
		printf("%d. dizi elemanini giriniz",i+1);
		scanf("%d",&A[i]);
	}
	
	for(i=0;i<n;i++)
	{
		toplam=toplam+A[i];
	}
	ort=toplam/n;
	a=0;
	b=0;
	for(i=0;i<n;i++)
	{
		if (A[i]>ort)
		{
			C[a]=A[i];
			a++;
		}
		else if(A[i]<ort)
		{
			B[b]=A[i];
			b++;
		}
	}
for(i=0;i<a;i++)
	{
		printf("%d ",C[i]);
	}
	return 0;
}