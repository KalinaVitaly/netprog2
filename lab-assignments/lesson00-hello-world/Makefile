
CC ?= $(CROSS_COMPILE)gcc
CFLAGS += -O2 -Wall -g

APPS = lab_00

all: $(APPS)

$(APPS): lab_00.o
	$(CC) -o $@ $^ $(LDFLAGS) $(LIBS)

%.o: %.c
	$(CC) $(CPPFLAGS) $(CFLAGS) -o $@ -c $<

clean:
	rm -f *.o $(APPS)
