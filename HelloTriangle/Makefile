CFLAGS = -D NDEBUG -std=c++17 -O2

CFLAGSD = -g -std=c++17  

LDFLAGS = -lglfw -lvulkan -ldl -lpthread -lX11 -lXxf86vm -lXrandr -lXi

VulkanTest: main.cpp
	g++ $(CFLAGS) -o VulkanTest main.cpp $(LDFLAGS)

VulkanDebug: main.cpp
	g++ $(CFLAGSD) -o VulkanDebug main.cpp $(LDFLAGS)

.PHONY: test clean

test: VulkanTest
	./VulkanTest

debug: VulkanDebug
	./VulkanDebug

clean:
	rm -f VulkanTest
