C=g++ 
CFLAGS=-g -Wall -I. -I/usr/X11/include
LDFLAGS= -lstdc++ -L /usr/X11R6/lib/ -L /Developer/SDKs/MacOSX10.6.sdk/usr/X11/lib/ -lglut -lGL -lGLU -lX11 -lXmu -lXi -lm -L /usr/lib -lpng12 -lz
SOURCES=outputScene.cpp include/glm/glm.cpp
OBJECTS=$(SOURCES:.cpp=.o)
EXECUTABLE=test

all: $(SOURCES) $(EXECUTABLE)
	
$(EXECUTABLE): $(OBJECTS) 
	$(CC) $(LDFLAGS) $(OBJECTS) -o $@

.cpp.o:
	$(CC) -c $(CFLAGS) $< -o $@

clean:
	@rm -f $(EXECUTABLE) $(OBJECTS)
