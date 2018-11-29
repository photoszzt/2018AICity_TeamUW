CXXFLAGS=-std=c++11 -g -Wall -fPIC -O3 -D_GLIBCXX_USE_CXX11_ABI=0
CXXFLAGS+=-I${CONDA_PREFIX}/include/
LDFLAGS=-L${CONDA_PREFIX}/lib -lopencv_core  -lopencv_highgui -lopencv_imgproc -lopencv_imgcodecs -lopencv_objdetect -lpng -ljpeg -ljasper -lz
CXX = g++
SOURCE = main.cpp

OBJECTS = $(SOURCE:.cpp=.o)
EXECUTABLE = main

all: $(EXECUTABLE)

%.o: %.cpp
	$(CXX) -o $@ -c $< $(CXXFLAGS)

$(EXECUTABLE): $(OBJECTS)
	$(CXX) -o $@ $< $(CXXFLAGS) $(LDFLAGS) 

clean:
	rm $(OBJECTS) $(EXECUTABLE)
