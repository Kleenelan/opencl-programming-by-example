Instances := sobel gaussian median

all: sobel gaussian median


%: %.cpp ../common/Timer.cpp ../common/bmp_image.cpp
	g++ $^ -I../include/ -L/opt/rocm-5.4.3/opencl/lib/libOpenCL.so -lOpenCL -o $@

.PHONY: clean
clean:
	rm -f ${Instances}
