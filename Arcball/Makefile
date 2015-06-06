INCLUDES = -I./ -I/usr/local/include/ -I/usr/include
LIBS = -L/usr/local/lib/ -L/usr/lib
LDLIBS = -lGL -lglfw -lGLEW
CXXFLAGS = -Wall -std=c++11

SOURCE = main.cpp
OBJECTS = ./Arcball.o 	\
		  ./Shader.o	\
		  ./Util.o

main: lib.a $(SOURCE)
	$(CXX) $(CXXFLAGS) $(SOURCE) $(INCLUDES) $(LIBS) $(LDLIBS) -o $@ $<

lib.a: $(OBJECTS)
	$(AR) rvs $@ $^

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c -o $@ $<

.PHONY: clean

clean:
	find . -name "*.0" -delete &\ 
	find . -name "main" -delete
