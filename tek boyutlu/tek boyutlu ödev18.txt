#include <stdio.h>
#include <math.h>

double aritmetik(int n ,double x[n] , double w[n]) 
{
  double top = 0;
  double agirlik = 0;
  for (int i = 0; i < n; i++) {
    top += x[i] * w[i];
    agirlik += w[i];
  }
  return top / agirlik;
}

double geometrik(int n, double x[n], double w[n]) {
  double carp = 1;
  double agirlik = 0;
  for (int i = 0; i < n; i++) {
    carp *= x[i];
    agirlik += w[i];
  }
  return pow(carp, 1.0 / agirlik);
}

double harmonik(int n, double x[n], double w[n]) {
  double top = 0;
  double agirlik = 0;
  for (int i = 0; i < n; i++) {
    top += w[i] / x[i];
    agirlik+= w[i];
  }
  return agirlik / top;
}

int main(void) {
  int n;
  printf("Eleman sayısını giriniz : ");
  scanf("%d", &n);

  double x[n];
  printf("Dizinin elemanlarını sirasiyla giriniz : ");
  for (int i = 0; i < n; i++) {
    scanf("%lf", &x[i]);
  }

  double w[n];
  printf("Elemanların agırlıklarini sirasiyla giriniz : ");
  for (int i = 0; i < n; i++) {
    scanf("%lf", &w[i]);
  }
printf("Agırlikli Aritmetik ortalama : %lf\n", aritmetik(n, x, w));
printf("Agirlikli Geometrik ortalama : %lf\n", geometrik(n, x, w));
printf("Agirlikli harmonik : %lf\n", harmonik(n, x, w));
return 0;
}
