Examples := profiling_saxpy

all: profiling_saxpy

%: %.cpp
	g++ $^ -I../include/ -L/opt/rocm-5.4.3/opencl/lib/libOpenCL.so -lOpenCL -o $@

.PHONY:clean
clean:
	rm -f ${Examples}
