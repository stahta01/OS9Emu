TARGET=os9emu
CPPFLAGS=-g -I/sw/include/root
LDFLAGS=-g
LDLIBS=
SOURCES=$(wildcard *.cc)
OBJS=$(SOURCES:.cc=.o)
SOURCES2=$(wildcard *.cpp)
OBJS2=$(SOURCES2:.cpp=.o)

$(TARGET): $(OBJS) $(OBJS2)
	g++ $(LDFLAGS) -o $@ $^ $(LDLIBS)

%.o: %.c[c,cp]
	g++ $(CPPFLAGS) -c $< -o $@

install:
	cp $(TARGET) /usr/local/bin

clean:
	rm -f $(TARGET) *.o
