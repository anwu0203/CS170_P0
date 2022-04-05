CC      = gcc
CFLAGS  = -O
LDFLAGS  = -O 


all: shell simple

testall:  test1 test2 test3 test4

testgs:  testgradescope

shell:  shell.o
	$(CC) -o $@ $^ $(LDFLAGS)

simple:  simple_shell.o
	$(CC) -o $@ $^ $(LDFLAGS)

.c.o:
	$(CC)  $(CFLAGS) -c $<

runsimple: 
	./simple

run: 
	./shell

test: 
	./shell < testfile

testsimple: 
	./simple < testfile

test1: 
	./shell < testfile1

test2: 
	./shell < testfile2

test3: 
	./shell < testfile3

test4: 
	./shell < testfile4

GS= gradescope_test
MAKE=make 

testgradescope: 
	$(MAKE) -C gradescope_test
	
clean:
	rm *.o
	rm shell
	rm simple
