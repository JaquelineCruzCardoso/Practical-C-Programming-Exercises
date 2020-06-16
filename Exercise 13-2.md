# Practical-C-Programming-Exercises
//*Exercise 13-2: Write a function that takes a single string as its argument and returns a pointer to the first nonwhite character in the string*//

#include <stdio.h>
#include <string.h>
char *nonwhite(char *thestring) {
	while ((thestring[0] == ' ') || (thestring[0] == '\t')) {
		++thestring;
	}

	return thestring;
}

int main() {

	char line[100];

	printf("String: ");
	fgets(line, sizeof(line), stdin);

	printf("Result: %s",nonwhite(line));
	return(0);
}
