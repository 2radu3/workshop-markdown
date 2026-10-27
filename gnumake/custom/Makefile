# --- Variables ---
# Requirement: Two variables (for compilers and flags)
# Added -I. to tell the compiler to look for header.h in the current directory
CC = gcc
CFLAGS = -Wall -g -I.

# --- Conditional Block ---
# Requirement: A conditional block
ifeq ($(shell uname), Linux)
    OS_MSG = "Running on Linux"
else
    OS_MSG = "Running on a non-Linux system"
endif

# --- Function ---
# Requirement: A function
define print_status
        @echo "[STATUS] $(1)"
endef

# --- Phony Rules ---
# Requirement: Declaration of all phony rules
.PHONY: all clean greet compile_parts

# --- Rules ---

# Requirement: an all rule (at the beginning of the file)
# Behaviour: Runs the greeting and parts compilation. Result: Builds the whole project.
all: greet compile_parts
        $(call print_status, "Everything built successfully!")

# Requirement: a rule for greeting.c
# Behaviour: Compiles greeting.c into a binary. Result: Creates 'greeting' executable.
greet: greeting.c
        $(call print_status, "Compiling greeting...")
        $(CC) $(CFLAGS) -o greeting greeting.c

# Requirement: a rule for compiling part1.c and part2.c (and using header.h)
# Behaviour: Compiles both C files and links them using the header.
# Result: Creates 'app' executable in one single command.
compile_parts: part1.c part2.c header.h
        $(call print_status, "Ch header.h...")
        $(CC) $(CFLAGS) part1.c part2.c -o app

# Requirement: a clean rule
# Behaviour: Removes all generans the workspace.
clean:
        $(call print_status, "C
        rm -f greeting app
        $(MAKE) -f extra.mk cle

# Requirement: Included/Referen
include extra.mk
