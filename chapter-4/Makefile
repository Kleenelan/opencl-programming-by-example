Instances := getSupportedImageFormats histogram_image image_sampler

all: getSupportedImageFormats histogram_image image_sampler

%: %.cpp
	g++ $^ -I../include/ -L/opt/rocm-5.4.3/opencl/lib/libOpenCL.so -lOpenCL -o $@


histogram_image: histogram_image.cpp ../common/bmp_image.cpp
	g++ $^ -I../include/ -L/opt/rocm-5.4.3/opencl/lib/libOpenCL.so -lOpenCL -o $@
image_sampler: image_sampler.cpp ../common/bmp_image.cpp
	g++ $^ -I../include/ -L/opt/rocm-5.4.3/opencl/lib/libOpenCL.so -lOpenCL -o $@
getSupportedImageFormats: getSupportedImageFormats.cpp ../common/bmp_image.cpp
	g++ $^ -I../include/ -L/opt/rocm-5.4.3/opencl/lib/libOpenCL.so -lOpenCL -o $@

.PHONY: clean
clean:
	rm -f ${Instances}
