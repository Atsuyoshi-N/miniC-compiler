CFLAGS=-std=c11 -g -static -fno-common
SRCS=$(wildcard *.c)
OBJS=$(SRCS:.c=.o)

9cc: $(OBJS)
	$(CC) -o $@ $(OBJS) $(LDFLAGS)

$(OBJS): 9cc.h

9cc-gen2: 9cc ${SRCS} 9cc.h
	./self.sh

extern.o: tests-extern
	gcc -xc -c -o extern.o tests-extern

test: 9cc
	./9cc tests > tmp.s
	gcc -static -o tmp tmp.s extern.o
	./tmp

test-gen2: 9cc-gen2 extern.o
	./9cc-gen2 tests > tmp.s
	gcc -static -o tmp tmp.s extern.o
	./tmp

clean:
	rm -rf 9cc 9cc-gen* *.o *~ tmp*

.PHONY: test clean
