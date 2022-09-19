CC=gcc

CFILES=main.c a_functions.c b_functions.c c_functions.c d_functions.c
OBJECTS=main.o a_functions.o b_functions.o c_functions.o d_functions.o
DEPFILES=main.h a.h b.h c.h d.h
EXE=program1
INSTDIR= /usr/local/bin

all: program1

$(EXE): $(OBJECTS)
	$(CC) -o $(EXE) $(OBJECTS)

main.o: main.c main.h
	$(CC) -c main.c

a_functions.o: a_functions.c a.h
	$(CC) -c a_functions.c

b_functions.o: b_functions.c b.h
	$(CC) -c b_functions.c

c_functions.o: c_functions.c c.h
	$(CC) -c c_functions.c

d_functions.o: d_functions.c d.h
	$(CC) -c d_functions.c

clean:
	rm -rf program1 $(OBJECTS)

install:
	mv $(EXE) $(INSTDIR)

uninstall:
	rm $(INSTDIR)/$(EXE)
