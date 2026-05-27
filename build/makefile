#
# makefile for TINY
# Borland C Version
# K. Louden 2/3/98
#
# modified at Oct. 29, 2022 in SJTU
#

CC = gcc

CFLAGS =

oS = main.o util.o scanner.o

main.o: ../main.c ../globals.h ../util.h ../scan.h
	$(CC) $(CFLAGS) -c ../main.c

scanner.o: ../scanner.c ../scan.h ../util.h ../globals.h
	$(CC) $(CFLAGS) -c ../scanner.c

util.o: ../util.c ../util.h ../globals.h
	$(CC) $(CFLAGS) -c ../util.c

clean:
	-rm main.o
	-rm util.o
	-rm scanner.o

rmelf:
	-rm bin/scanner
	-rm bin/parser

scanner: $(oS)
	$(CC) $(CFLAGS) -o bin/scanner $(oS)

tests:
	-bin/scanner test/sample.tny
