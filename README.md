# libft

> A compact re-implementation of core C standard library routines (42 School `libft`) built as a reusable static library.

![Language](https://img.shields.io/badge/language-C-blue)
![Build](https://img.shields.io/badge/build-Makefile-informational)
![Platform](https://img.shields.io/badge/platform-Linux%20%7C%20macOS-lightgrey)

## Overview

`libft` is a foundational C library that recreates a subset of common libc utilities (string/memory helpers, character checks, conversions) and adds a few convenience helpers frequently used in systems programming projects.

This repository is the classic *"build your own standard library"* exercise: it demonstrates low-level C skills (pointer arithmetic, memory safety, API design) while producing a practical artifact you can link into other projects.

**Repository:** `otelliq/libft`  
**Default branch:** `main`

## Key features

- **Libc re-implementations**: `ft_strlen`, `ft_memcpy`, `ft_strlcpy`, `ft_strncmp`, etc.
- **Character checks & transforms**: `ft_isalpha`, `ft_isdigit`, `ft_tolower`, `ft_toupper`
- **Memory helpers**: `ft_bzero`, `ft_calloc`, `ft_memset`, `ft_memmove`
- **String utilities**: `ft_substr`, `ft_strjoin`, `ft_strtrim`, `ft_split`
- **Conversions**: `ft_atoi`, `ft_itoa`
- **FD-based output**: `ft_putchar_fd`, `ft_putstr_fd`, `ft_putendl_fd`, `ft_putnbr_fd`

(See the public API in `libft/libft.h`.)

## Screenshots

> No screenshots provided yet.

- Add images to a `docs/` or `assets/` folder and update this section.

## Installation / Setup

### Prerequisites

- `make`
- A C compiler (`cc`, `clang`, or `gcc`)

### Build the library

From the repository root:

```bash
make -C libft
```

This produces a static library (commonly `libft.a`) inside the `libft/` directory.

## Usage

### Link `libft` in another C project

1. Build `libft`:

```bash
make -C libft
```

2. Include the header and link the library:

```c
#include "libft.h"

int main(void)
{
    const char *s = "hello";
    return (int)ft_strlen(s);
}
```

Example compile command (adjust paths as needed):

```bash
cc -I ./libft your_program.c ./libft/libft.a -o your_program
```

## Project structure

```text
.
├── README.md
└── libft/
    ├── Makefile
    ├── libft.h
    └── ft_*.c
```

## License

No license file is currently included in this repository.

If you want this to be reusable by others, consider adding a `LICENSE` file (MIT/Apache-2.0 are common choices) and updating this section accordingly.
