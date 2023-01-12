#include <stdio.h>
#include <stdlib.h>

int main(void) {
  
  char cumle[100];

  char k=' ';
  int i;
  cumle[k]=' ';
  printf("Cumleyi yaziniz:");
  gets(cumle);
  
  for(i=0; cumle[i]!='\0';i++)
  {
  	if(cumle[i]==',' || cumle[i]=='.' || cumle[i]==':'  ||  cumle[i]==';' || cumle[i]=='?' || cumle[i]=='\'' || cumle[i]=='...' || cumle[i]=='!' || cumle[i]=='\"')
  	{
  	printf("%c",cumle[i]);
  	printf("%c",cumle[k]);
  }
  	else
  	printf("%c",cumle[i]);
  }
 

  
  return 0;
}