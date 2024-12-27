
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

| Format specifier | Data type                  |
| ---------------- | -------------------------- |
| %d               | int                        |
| %ld              | long                       |
| %lld             | long long                  |
| %lf              | double                     |
| %Lf              | long double                |
| %f               | float                      |
| %c               | char                       |
| %s               | string(array of char)      |
| %hi              | short                      |
| %hu              | unsigned short             |
| %p               | pointer(or memory address) |
| %u               | unsigned int               |
| %o               | octal                      |
| %x               | hexadecimal                |
"%.2f"  is used to print float numbers up to 2 decimal places.
"%6d" means increased width for integer.

![[Pasted image 20241227164919.png]]

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

Can also chain macros, one macro calling another macro is valid
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

##### Pre defined Macros
`__FILE__` - Current file name
`__LINE__` - Current line number
`__DATE__` - Compilation date (as string)
`__TIME__` - Compilation time (as string)

### Preprocessor Directives

##### 1. `ifdef` and `ifndef`
Used to include a section of code if a certain macro is defined or not defined.
Syntax:
```
#define DEBUG 1
#ifdef DEBUG
	printf("DEBUG mode is enabled");
#endif
#ifndef DEBUG
	printf("DEBUG mode is not enabled");
#endif
```
(`endif` is used to signify ending of `ifdef` `ifndef` blocks)
##### 2.  `if`,  `elif` and `else`
Same as if elif else from main program.
```
#if macro_condition  
   statements  
#elif macro_condition  
   statements  
#else
   statements  
#endif
```
##### 3. `error`
`error`  is used to abort compilation process and throw error.
```
#ifndef SOMEMACRO
	#error SOMEMACRO not found!
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

### Switch statement
`switch` is used to execute one condition from multiple conditions.
```
int var = 1;
switch(var) {
	case 1:
		printf("Var is 1");
		break;
	case 2:
		printf("Value of var is 2");
		break;
	default:
		printf("Value of var is unknown");
		break;
}
```
### Pointers
A pointer (\*) provides a reference to an entity of the referenced type. Also used as indirection or dereferencing operator.
```
int a=17;
int *p_a=&a //returns the memory address of variable a
```
Use `*` again on a pointer to get the value.
```
int value=*p_a;
```
Use `&` to turn value into pointer(by getting memory address)
Pointers can be used to reference arrays too. By default zeroth index is returned.
```
int a[10];
int i=*a; //value of 0th element in a
int j=*(a+1) //value of 2nd elmeent in a
```

