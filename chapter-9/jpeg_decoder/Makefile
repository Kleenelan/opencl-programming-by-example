Instances := JPEG_Decoder
#bitonic_sort parabolic_regression linear_regression dataForKNN knn_classification

all: JPEG_Decoder
#bitonic_sort parabolic_regression linear_regression dataForKNN knn_classification


%: *.cpp
	g++ $^ -I../../include/ -L/opt/rocm-5.4.3/opencl/lib/libOpenCL.so -lOpenCL -o $@

.PHONY: clean
clean:
	rm -f ${Instances}
