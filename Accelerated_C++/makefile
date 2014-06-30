SHELL=/bin/sh
CXX = g++
CC = g++
CHK_LINT = cppcheck
CHK_MEM = valgrind --tool=memcheck

SUBS = chapter00 chapter01 chapter02 chapter03 chapter04 \
	chapter05 chapter06 chapter07 chapter08 chapter09 \
	chapter10 chapter11 chapter12 chapter13 chapter14 \
	chapter15 chapter16

all:
	-for c in $(SUBS); do echo "=== $$c =="; (cd $$c; $(MAKE) "CXX=$(CXX)" "CC=$(CC)") done

test:
	-for c in $(SUBS); do echo "=== $$c =="; (cd $$c; $(MAKE) "CXX=$(CXX)" "CC=$(CC)" test); done

clobber:
	-for c in $(SUBS); do echo "=== $$c =="; (cd $$c; $(MAKE) "CXX=$(CXX)" "CC=$(CC)" clobber);done


checklint:
	-for c in $(SUBS); do echo "=== $$c =="; (cd $$c; $(MAKE) "CHK_LINT=$(CHK_LINT)" checklint);done


checkmem:
	-for c in $(SUBS); do echo "=== $$c =="; (cd $$c; $(MAKE) "CHK_MEM=$(CHK_MEM)" checkmem);done

