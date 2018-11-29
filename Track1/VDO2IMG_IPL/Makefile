CXXFLAGS=-std=c++11 -g -Wall -fPIC -O3 -D_GLIBCXX_USE_CXX11_ABI=0
CXXFLAGS+=-I${CONDA_PREFIX}/include/
LDFLAGS=-L${CONDA_PREFIX}/lib -lopencv_core -lopencv_videoio -lopencv_imgcodecs -lopencv_highgui
CXX = g++
SOURCE = src/main.cpp 

OBJECTS = $(SOURCE:.cpp=.o)
EXECUTABLE = vdo2img_ipl

all: $(EXECUTABLE)

%.o: %.cpp
	$(CXX) -o $@ -c $< $(CXXFLAGS)

$(EXECUTABLE): $(OBJECTS)
	$(CXX) -o $@ $^ $(CXXFLAGS) $(LDFLAGS) 

clean:
	rm $(OBJECTS) $(EXECUTABLE)
