CC=gcc
CFLAGS=-std=c2x -g -Wall

EXE_OBJ_COMMON=main.o $(LINK_COMMON)

.DEFAULT_GOAL := all

.PHONY: all
all: tinylisp-commented tinylisp-tested tinylisp tinylisp-opt

.PHONY: clean
clean: 
	find . -type f -perm /u+x -exec rm  {} \;
	rm -f *.o

tinylisp-tested: tinylisp-tested.o $(EXE_OBJ_COMMON)
	$(CC) $(CFLAGS) -o $@  $^