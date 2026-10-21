# myLib

A reusable C utility library containing string and memory helpers, character checks, number conversion, linked-list functions, formatted output, and line-by-line input.

## Contents

- Memory: allocation, zeroing, copy, move, comparison, and search.
- Strings: length, copy, concatenation, search, split, trim, and substring helpers.
- Conversion and character functions: integer parsing, integer-to-string, and character classification/case conversion.
- Linked lists: creation, insertion, traversal, mapping, and cleanup.
- Output: `ft_printf` and descriptor-based output helpers.
- Input: `get_next_line` and supporting functions.

Declarations and shared types are in `myLib.h`; implementations are in the root `.c` files.

## Build and link

Requirements: Make, a C compiler, and `ar`.

```sh
make
```

The Makefile targets `myLib.a` and uses `-Wall -Wextra -Werror`. Include `myLib.h` from your program and link the archive:

```sh
cc -Wall -Wextra -Werror main.c myLib.a -o example
```

The current Makefile's object rule refers to `libft.h`, while the committed public header is `myLib.h`. Review that prerequisite if your Make installation reports a header dependency problem; no header with the former name is included here.

## Cleanup

```sh
make clean   # Remove object files
make fclean  # Also remove myLib.a
make re      # Rebuild
```

This is a project utility library. Check each function's declaration and implementation before relying on behavior beyond the usual C-library-like operations.
