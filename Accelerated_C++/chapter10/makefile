CXX = g++
CC = g++
CHK_LINT = cppcheck
CHK_MEM = valgrind --tool=memcheck

TARGETS := concat_files copyfile pointer_example write_args

all: $(TARGETS)


test:		all
	./concat_files ../data/name1 ../data/name2
	./copyfile
	./pointer_example
	./write_args this is a test

clobber:
	rm -f *.o *.exe out in core $(TARGETS)

checkmem:
	for t in $(TARGETS); do echo -e "*** dcheck \"$$t\" ***"; $(CHK_MEM) ./$$t; done





