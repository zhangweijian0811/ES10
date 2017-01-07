#include <stdlib.h>
#include <stdio.h>
#include "es10.h"


void sum_fractions() {
	int a1, a2;
	int b1, b2;
	printf("Insert 1? fraction \n");
	scanf("%d",&a1);
	scanf("%d",&a2);
	while (a1>a2||a1==a2)
	{
		printf("Insert 1? fraction \n");
		scanf("%d", &a1);
		scanf("%d", &a2);
	}
	printf("Insert 2? fraction \n");
	scanf("%d", &b1);
	scanf("%d", &b2);
	while (b1 > b2 || b1 == b2)
	{
		printf("Insert 2? fraction \n");
		scanf("%d", &b1);
		scanf("%d", &b2);
	}
	int c1, c2;
	if (a2 == b2) {
		c2 = a2;
		c1 = a1 + b1;
	}
	if (a2!=b2) {
		c2 = a2*b2;
		c1 = (a1*b2) + (a2*b1);
	      }
	int i = 2;
	while (i<=c1&&i<=c2)
	{
		if (c1%i == 0 && c2%i == 0)
		{
			c1 = c1 / i;
			c2 = c2 / i;
		}
		else
		{
			++i;
		}
	}
	printf("Resulting fraction: %d/%d\n", c1, c2);
}

void find_k() {
	int m;
	printf("Insert a positive integer number greater than 0\n");
	scanf("%d", &m);
	while (m<=1)
	{
		printf("Insert a positive integer number greater than 0\n");
		scanf("%d", &m);
	}
	int n = 0;
	int k = 1;
	while (n<m)
	{   
		n = n + (k*k);
		if(n==m){
			printf("k = %d\n", k);
			break;
		}
		if (n > m) {
			--k;
			printf("k = %d\n", k);
			break;
		}
		k++;
	}
}

void print_sequence() {
	int n;
	printf("Insert a positive integer number greater than 0\n");
	scanf("%d", &n);
	while (n<1)
	{
		printf("Insert a positive integer number greater than 0\n");
		scanf("%d", &n);
	}
	int m = 1;	
	int q = 0;
	while (q < n) {
		q = m*m;
		if (q<=n)
		  { printf("%d\n", q); }
		++m;
	}
}
