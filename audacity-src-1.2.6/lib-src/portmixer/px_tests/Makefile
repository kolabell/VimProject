all: px_test

CFLAGS = -g -Wall -O -I../../portaudio/pa_common -I../px_common

px_test: px_test.o px_win_wmme.o ../px_common/portmixer.h
	gcc -g -o px_test px_test.o px_win_wmme.o -lm \
		-L../../portaudio/pa_win_wmme -lportaudio -lpthread

px_test.o: px_test.c ../px_common/portmixer.h
	gcc $(CFLAGS) -c px_test.c


px_win_wmme.o: ../px_win_wmme/px_win_wmme.c ../px_common/portmixer.h
	gcc $(CFLAGS) -c ../px_win_wmme/px_win_wmme.c


