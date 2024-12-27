
### Taking user input

```
#include <stdio.h>
int main(){
	int a;
	char s[10];
	scanf("%d", &a);
	scanf("%s",s);	
	printf("%d", a);
	return 0;
}

```
Alternatively `getchar` can also be used to get one single character from user but this is not recommended due to security vulnerabilities.
![[Pasted image 20241227171526.png]]

| Format specifier | Data type             |
| ---------------- | --------------------- |
| %d               | int                   |
| %ld              | long                  |
| %lld             | long long             |
| %lf              | double                |
| %Lf              | long double           |
| %f               | float                 |
| %c               | char                  |
| %s               | string(array of char) |
| %hi              | short                 |
| %hu              | unsigned short        |
| %p               | pointer               |
| %u               | unsigned int          |
| %o               | octal                 |
| %x               | hexadecimal           |
"%.2f"  is used to print float numbers up to 2 decimal places.
"%6d" means increased width for integer.![[Pasted image 20241227164919.png]]

### Macros

##### Using for variables

```
#include <stdio.h>
#define MAX 10

int main(){
	int n=MAX;
	printf("Max is: %d", n);
	return 0;
}
```
##### Using for functions 

```
#include <stdio.h>
#define AREA(l, b) (l*b)

int main() {
	int l, b;
	scanf("%d %d", &l, &b);
	printf("Area is: %d", AREA(l, b));
	return 0;
}
```

Can also chain macros, one macro calling another macro is valid.
##### Multi line macro

```
#include <stdio.h>
#define ELE 1, \
			2, \
			3
int main() {
	int arr[] = { ELE };
	...
	return 0;
}
```

### Compilation steps

##### 1. Pre processing
Handles directives like include and define
##### 2. Compilation
Translates C code to Assembly
##### 3. Assembly
Assembler converts assembly code into pure binary code.
##### 4. Linking
Linker merges all the object code from multiple modules into one.

### Comments

```
//this is a single line comment
/* this
is a multi line
comment */
```

### Variable naming rules

1. Start with letter or underscore
2. Can have digits, letters or underscores
3. Case sensitive
4. No whitespaces 

### Variable 

1. Global
2. Local
3. Static
4. Register

```
// Global Variable
int globalVar;
void function() {
	// Local Variable
	int localVar;
	// Static Variable
	static int staticVar = 0;
	staticVar++;
	// Register Variable
	for(register int i = 0; i < 10; i++) {
	// Fast access within loop
	}
}
```

### Data types

![[c_datatypes.jpg]]
![[c_datatypes_sizes.png]]
long double can be 12 **or** 16 bytes.

### Operators

![[Operators-in-C.png]]

When comparing unsigned int with signed, the signed int is automatically converted to unsigned for comparison purposes.

### Escape sequences

| Sequence | Function               |
| -------- | ---------------------- |
| \n       | New line               |
| \t       | Tab space              |
| \\"      | To print double quotes |
| \\'      | To print single quotes |

