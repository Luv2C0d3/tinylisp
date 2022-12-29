CC=gcc
CFLAGS=-std=c2x -g -Wall
#CFLAGS.test-tl-commented += -DDEBUG

#LINK_COMMON=lex.o
TEST_OBJ_COMMON=../test-framework/unity.o test-util.o $(LINK_COMMON)
EXE_OBJ_COMMON=../src/main.o $(LINK_COMMON)

.DEFAULT_GOAL := all

.PHONY: all
all: test-tl-tested 

# tinylisp-float tinylisp-float-opt
.PHONY: clean
clean: 
	find . -type f -perm /u+x -exec rm  {} \;
	rm -f *.o

test-tl-tested: test-tl-tested.o ../src/tinylisp-tested.o $(TEST_OBJ_COMMON)
	$(CC) $(CFLAGS) -o $@  $^


