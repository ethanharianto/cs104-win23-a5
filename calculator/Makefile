# Compiler
CC = gcc

# Compiler flags
CFLAGS = -Wall -Werror -std=c99 -g

# Source files
SRC = main.c addition.c subtraction.c multiplication.c division.c

# Object files (replace .c with .o)
OBJ = $(SRC:.c=.o)

# Executable name
TARGET = calculator

# Default rule (builds the calculator)
all: $(TARGET)

# Link object files into the executable
$(TARGET): $(OBJ)
	$(CC) $(CFLAGS) -o $(TARGET) $(OBJ)

# Compile each .c file into a .o file
%.o: %.c operations.h
	$(CC) $(CFLAGS) -c $< -o $@

# Clean rule to remove object files and the executable
clean:
	rm -f $(OBJ) $(TARGET)
