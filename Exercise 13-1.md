# Practical-C-Programming-Exercises
//*Exercise 13-1: Write a program that uses pointers to set each element of an array to zero.*//
#include <stdio.h>
#define Array_Max 36

int val[Array_Max] = 
{            
	9,8,7,6,5,4,3,2,1,0,1,2,3,4,5,6,7,8,1,4,7,2,5,
	8,3,6,9,-9,-8,-7,-6,-5,-4,-3,-2,-1
};

int N;                     
int *val_ptr;            
int main() {

	for (N = 0; N < Array_Max; ++N) {
		printf("values[%d] = %d\n", N, val[N]);
	}
	val_ptr = &val[0];
	for (N = 0; N < Array_Max; ++N) {
		*val_ptr = 0;
		++val_ptr;
	}
	printf("\n\n-----------------------------------\n Here start the new array\n\n");
	for (N = 0; N < Array_Max; ++N) {
		printf("values[%d] = %d\n", N, val[N]);
	}
	return(0);
}
