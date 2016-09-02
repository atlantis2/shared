.SUFFIXES: .c .o


OBJS =


CC = gcc
OPTS = -g -O2
OPTS +=-Wimplicit -Wreturn-type -Wunused -Wuninitialized -Wparentheses \
		-Wpointer-arith -Wendif-labels -Wundef -Wcast-align -Wformat-security \
		-Wmissing-format-attribute -DINSTALL_PATH=\"$(INSTALL_PATH)\"
INCS = 
LIBS = 
HASHLIBS =
CFLAGS  = $(OPTS) $(INCS) $(LIBS)
TARGETDIR = ${INSTALL_PATH}/sbin/sys
TARGET = echoserver

all: $(TARGET)

clean:
	rm -f *.o $(TARGET) *.core tags
	
tags: 
	ctags -Rw ./

indent:
	./Lindent *.c
	rm -rf *~

new : 
	$(MAKE) clean 
	$(MAKE)

echoserver: echoserver.o
	$(CC) $(OPTS) $(LDFLAGS) -o $@ $@.o $(LIBS)

	


