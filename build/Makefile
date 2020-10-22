CXX = g++
RM = rm
SRC = ../src
CXXFLAGS = -Wall -O2 -fPIC -pipe -std=c++11 -I$(SRC)
SRCS = $(wildcard $(SRC)/*.cpp)
OBJS = $(patsubst %cpp,%o,$(notdir $(SRCS)))
TARGET = fs

$(TARGET) : $(OBJS)
	$(CXX) $(OBJS) -o $@

$(OBJS) : %.o : $(SRC)/%.cpp
	$(CXX) $(CXXFLAGS) -c -o $@ $^

.PHONY : all clean

all : $(TARGET)

clean: 
	$(RM) *.o $(TARGET)
