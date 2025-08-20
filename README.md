# 🚀 Libft - The Foundation of 42 Excellence

<div align="center">

[![42 School](https://img.shields.io/badge/42-School-000000?style=for-the-badge&logo=42&logoColor=white)](https://42.fr/)
[![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=white)](https://en.wikipedia.org/wiki/C_(programming_language))
[![Norminette](https://img.shields.io/badge/Norminette-✅_Passing-success?style=for-the-badge)](https://github.com/42School/norminette)
[![Grade](https://img.shields.io/badge/Grade-125%2F100-brightgreen?style=for-the-badge)]()

*"Your very first own library"*

</div>

---

## 🎯 What is Libft?

**Libft** is the first milestone in every 42 student's journey. It's where you rebuild the wheel to understand how the wheel works. This project challenges you to recreate essential C standard library functions from scratch, giving you deep insights into memory management, algorithms, and the inner workings of C.

> *"It's not about the destination, it's about the journey of understanding every byte."*

## ✨ Why This Matters

- 🧠 **Deep Understanding**: Learn how fundamental functions actually work under the hood
- 🛠️ **Foundation Building**: Every future 42 project builds upon this library
- 💪 **Memory Mastery**: Master dynamic allocation and pointer manipulation
- 🎯 **Algorithm Thinking**: Develop efficient problem-solving patterns
- 🔧 **Tool Creation**: Build your own toolkit that you'll use throughout 42

---

## 📚 Function Arsenal

### 🔤 Character Classification & Transformation
Functions that analyze and transform individual characters.

| Function | Purpose | What It Does |
|----------|---------|--------------|
| `ft_isalpha` | Letter check | Is it a-z or A-Z? |
| `ft_isdigit` | Digit check | Is it 0-9? |
| `ft_isalnum` | Alphanumeric check | Letter or digit? |
| `ft_isascii` | ASCII check | Valid ASCII character? |
| `ft_isprint` | Printable check | Can you see it when printed? |
| `ft_toupper` | Case conversion | Make it LOUD |
| `ft_tolower` | Case conversion | make it quiet |

### 🧵 String Manipulation Wizardry
The bread and butter of C programming - string operations.

| Function | Purpose | Superpower |
|----------|---------|------------|
| `ft_strlen` | Length calculation | Count every character |
| `ft_strchr` | Character hunting | Find first occurrence |
| `ft_strrchr` | Reverse hunting | Find last occurrence |
| `ft_strncmp` | String comparison | Who comes first alphabetically? |
| `ft_strnstr` | Substring search | Find needle in haystack |
| `ft_strlcpy` | Safe copying | Copy without buffer overflow |
| `ft_strlcat` | Safe concatenation | Join strings safely |
| `ft_strdup` | String duplication | Clone a string |
| `ft_substr` | Substring extraction | Cut out a piece |
| `ft_strjoin` | String fusion | Merge two strings |
| `ft_strtrim` | String trimming | Remove unwanted characters |
| `ft_split` | String splitting | Break it into pieces |
| `ft_strmapi` | String mapping | Transform each character |
| `ft_striteri` | String iteration | Apply function to each char |

### 🧠 Memory Management Magic
Direct memory manipulation - the core of C power.

| Function | Purpose | Memory Superpower |
|----------|---------|-------------------|
| `ft_memset` | Memory filling | Paint memory with a value |
| `ft_bzero` | Memory zeroing | Clean slate |
| `ft_memcpy` | Memory copying | Duplicate memory blocks |
| `ft_memmove` | Safe memory move | Copy even with overlap |
| `ft_memchr` | Memory scanning | Find byte in memory |
| `ft_memcmp` | Memory comparison | Compare memory blocks |
| `ft_calloc` | Clean allocation | Allocate and initialize |

### 🔄 Conversion Utilities
Transform data between different representations.

| Function | Purpose | Transformation |
|----------|---------|----------------|
| `ft_atoi` | String to integer | "42" → 42 |
| `ft_itoa` | Integer to string | 42 → "42" |

### 📁 File Descriptor Operations
Direct output to files, terminals, and more.

| Function | Purpose | Output Target |
|----------|---------|---------------|
| `ft_putchar_fd` | Character output | Single character anywhere |
| `ft_putstr_fd` | String output | Full string anywhere |
| `ft_putendl_fd` | String + newline | String with automatic newline |
| `ft_putnbr_fd` | Number output | Integer anywhere |

---

## 🚀 Quick Start

```bash
# Clone this masterpiece
git clone git@github.com:danielgessner/42_Core_libft.git
cd 42_Core_libft

# Build the library
make

# Include in your project
#include "libft.h"
```

## 💡 Usage Examples

### String Magic
```c
#include "libft.h"

int main(void)
{
    // Create and manipulate strings
    char *greeting = ft_strdup("Hello, 42!");
    char *upper = ft_strmapi(greeting, char_to_upper);
    
    // Split text into words
    char **words = ft_split("Welcome to 42 School", ' ');
    
    // Join them back with a different separator
    char *result = ft_strjoin(words[0], " - ");
    result = ft_strjoin(result, words[2]);
    
    ft_putendl_fd(result, 1); // "Welcome - 42"
    
    return (0);
}
```

### Memory Mastery
```c
// Allocate and initialize memory
char *buffer = ft_calloc(100, sizeof(char));

// Fill with pattern
ft_memset(buffer, 'A', 50);

// Safe memory operations
ft_memmove(buffer + 10, buffer, 40);
```

### Number Conversion
```c
// String to number and back
int number = ft_atoi("42");
char *str = ft_itoa(number * 2);
ft_putstr_fd(str, 1); // "84"
```

---

## 🛠️ Build System

### Makefile Targets
```bash
make        # Build libft.a
make clean  # Remove object files
make fclean # Remove everything
make re     # Rebuild from scratch
make bonus  # Build with bonus functions
```

### Compilation Flags
- `-Wall` - All common warnings
- `-Wextra` - Extra warnings  
- `-Werror` - Warnings become errors

---

## 🧪 Testing Your Library

### Recommended Testers
- **[libft-unit-test](https://github.com/alelievr/libft-unit-test)** - Comprehensive unit tests
- **[libftest](https://github.com/jtoty/libftest)** - Classic libft tester
- **[francinette](https://github.com/xicodomingues/francinette)** - The 42 student's best friend

```bash
# Quick test with libft-unit-test
git clone https://github.com/alelievr/libft-unit-test.git
cd libft-unit-test
make f
```

---

## 📋 42 Standards Compliance

### ✅ Norminette Perfect
- Maximum 25 lines per function
- Maximum 5 functions per file  
- No forbidden keywords (`for`, `switch`, `case`, `goto`)
- Proper 42 header format
- No global variables
- Perfect indentation and spacing

### 🎯 Project Requirements
- **Language**: C
- **Standard**: C99
- **Forbidden**: Most stdlib functions
- **Memory**: Zero leaks, proper management
- **Style**: 42 Norminette compliance

---

## 🏆 Project Stats

- **Functions Implemented**: 34
- **Lines of Code**: ~2000
- **Time Investment**: 40+ hours
- **Learning Value**: Immeasurable
- **Future Impact**: Foundation for everything

---

## 🌟 What Makes This Special

This isn't just a library - it's a **learning journey**. Every function has been:

- ✨ **Carefully crafted** with attention to edge cases
- 🧪 **Thoroughly tested** against multiple test suites  
- 📚 **Well documented** for future reference
- 🎯 **Optimized** for both readability and performance
- ❤️ **Built with passion** for the craft of programming

---

## 🚀 Beyond Libft

This library becomes your companion throughout 42:
- **ft_printf**: Extended with your own printf
- **get_next_line**: File reading utilities
- **push_swap**: Algorithm challenges
- **minishell**: Command line interfaces
- **And beyond**: Every project builds on this foundation

---

## 📖 Philosophy

> *"The best way to understand something is to build it yourself."*

Libft embodies the 42 philosophy of learning by doing. It's not about copying existing functions - it's about understanding the fundamental patterns of programming, memory management, and algorithm design that will serve you throughout your career.

---

<div align="center">

**Made with ❤️ at 42 Heilbronn**

*Where peer learning meets technical excellence*

---

*"Code is poetry written in logic"*

</div>