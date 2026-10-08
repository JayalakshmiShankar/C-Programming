# C Programming: Part 1, Introduction

## 1. What is C and why does it exist?

Before C, programmers had two choices: **assembly** (full control but hard to read and tied to one machine) or high-level languages (easier but too slow for building an operating system). C was made to be **readable and close to the hardware**.

| Year | Language | Note |
| ---- | -------- | ---- |
| 1967 | BCPL | Simple language for writing compilers |
| 1969 | B | Ken Thompson's smaller version, used for early Unix |
| 1972 | C | Dennis Ritchie at Bell Labs added data types and structure |
| 1973 | Unix rewritten in C | An OS could now move to new machines by recompiling |

**Where C is used today:** operating systems (Linux), embedded systems, databases (SQLite), and language runtimes. The standard Python interpreter is written in C, and libraries like NumPy are fast because their heavy parts are written in C.

---

## 2. Compiled language: how your code runs

Your CPU only understands machine code, so a **compiler** translates your whole C program first, and then you run the result.

1. **Preprocessing:** handles lines starting with `#` (like `#include`)
2. **Compilation:** converts C into assembly
3. **Assembly:** converts assembly into machine code (an object file)
4. **Linking:** joins your code with library code (like `printf`) to make the executable

```bash
gcc -std=c11 -Wall -Wextra -pedantic hello.c -o hello
./hello          # Windows PowerShell: .\hello.exe
```

The flags `-Wall -Wextra -pedantic` turn on helpful warnings. Always use them.

---

## 3. Example problems (solved)

### Example 1: Hello, World

```c
#include <stdio.h>

int main(void) {
    printf("Hello, World!\n");
    return 0;
}
```

Output:

```
Hello, World!
```

| Line | Meaning |
| ---- | ------- |
| `#include <stdio.h>` | Brings in the input/output library so `printf` works |
| `int main(void)` | Every C program starts from `main` |
| `printf(...)` | Prints text. `\n` means new line |
| `return 0;` | Tells the OS the program ended successfully |

---

### Example 2: Print your details

```c
#include <stdio.h>

int main(void) {
    printf("Name   : Asha\n");
    printf("College: ABC Institute of Technology\n");
    printf("Branch : Computer Science\n");
    return 0;
}
```

Output:

```
Name   : Asha
College: ABC Institute of Technology
Branch : Computer Science
```

---

### Example 3: Read a name and greet

```c
#include <stdio.h>

int main(void) {
    char name[50];

    printf("What is your name? ");
    fgets(name, sizeof(name), stdin);

    printf("Hello, %s", name);
    return 0;
}
```

Output (what you type is `Jaya`):

```
What is your name? Jaya
Hello, Jaya
```

In C you choose the size of the text storage yourself (`name[50]`). `fgets` keeps the newline you typed, which is why the output has no `\n` after `%s`.

---

### Example 4: Add two numbers

```c
#include <stdio.h>

int main(void) {
    int a, b;

    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    printf("Sum = %d\n", a + b);
    return 0;
}
```

Output (you type `12 30`):

```
Enter two numbers: 12 30
Sum = 42
```

- `%d` is the placeholder for an integer.
- `&a` means "the address of `a`", so `scanf` knows where to store the value. This makes full sense once you learn pointers.

---

### Example 5: Sum, difference and product

```c
#include <stdio.h>

int main(void) {
    int a, b;

    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    printf("Sum        = %d\n", a + b);
    printf("Difference = %d\n", a - b);
    printf("Product    = %d\n", a * b);
    return 0;
}
```

Output (you type `12 5`):

```
Enter two numbers: 12 5
Sum        = 17
Difference = 7
Product    = 60
```

---

### Example 6: Name and age

```c
#include <stdio.h>

int main(void) {
    char name[50];
    int age;

    printf("Enter your name: ");
    scanf("%49s", name);
    printf("Enter your age: ");
    scanf("%d", &age);

    printf("Hi %s, next year you will be %d.\n", name, age + 1);
    return 0;
}
```

Output (you type `Jaya` and `18`):

```
Enter your name: Jaya
Enter your age: 18
Hi Jaya, next year you will be 19.
```

`%49s` limits the input to 49 characters so it cannot overflow the 50-character array. Note that `%s` stops at the first space, so this works for a single-word name only.

---

## 4. Common mistakes

| Mistake | What happens |
| ------- | ------------ |
| Missing semicolon | Compile error: `expected ';' before ...` |
| Forgetting `#include <stdio.h>` | Warning or error about `printf` |
| Missing `\n` | Output runs into the next terminal line |
| Writing `Main` instead of `main` | Linker error: C is case-sensitive |
| Forgetting `&` in `scanf` | Crash or unpredictable behavior |

**Bug hunt:** what is wrong here?

```c
#include <stdio.h>

int main(void) {
    printf("Hello, World!\n")
    return 0;
}
```

Answer: the `printf` line is missing a semicolon. The compiler reports `error: expected ';' before 'return'`. The error often points at the line after the real mistake.

---

## 5. Practice problems

1. Print your own name, college and branch on three lines.
2. Read two numbers and print their sum, difference and product.
3. Read a name and age and print: `Hi <name>, next year you will be <age + 1>.`
4. Run `gcc -S hello.c` and open `hello.s`. Write 2-3 sentences on what you notice.
5. Pick any language from the timeline in section 1. Write 2-3 sentences on what problem it solved and what limitation it had.

---

**Next:** Part 2, Variables, Data Types and Operators.