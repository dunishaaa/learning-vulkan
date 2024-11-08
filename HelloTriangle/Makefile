CFLAGS = -D NDEBUG -std=c++17 -O2

CFLAGSD = -g -std=c++17  

LDFLAGS = -lglfw -lvulkan -ldl -lpthread -lX11 -lXxf86vm -lXrandr -lXi

FILES = main.cpp HelloTriangleApplication.cpp

VulkanTest: main.cpp HelloTriangleApplication.cpp
	g++ $(CFLAGS) -o VulkanTest $(FILES) $(LDFLAGS)

VulkanDebug: main.cpp HelloTriangleApplication.cpp
	g++ $(CFLAGSD) -o VulkanDebug $(FILES) $(LDFLAGS)

.PHONY: test clean

VulkanTuto:
	g++ $(CFLAGS) -o VulkanTuto main1.cpp $(LDFLAGS)


test: VulkanTest
	./VulkanTest

debug: VulkanDebug
	./VulkanDebug

tuto: VulkanTuto
	./VulkanTuto

clean:
	rm -f VulkanTest VulkanDebug VulkanTuto
