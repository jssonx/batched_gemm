# GENCODE_FLAGS = -gencode arch=compute_30,code=sm_30 -gencode arch=compute_35,code=sm_35 -gencode arch=compute_37,code=sm_37 -gencode arch=compute_50,code=sm_50 -gencode arch=compute_52,code=sm_52 -gencode arch=compute_60,code=sm_60 -gencode arch=compute_61,code=sm_61 -gencode arch=compute_70,code=sm_70 -gencode arch=compute_70,code=compute_70
GENCODE_FLAGS =  -gencode arch=compute_80,code=compute_80

gemm:gemm.cu
	nvcc  $< -o $@ --std=c++11 -O3 -lcublas ${GENCODE_FLAGS}
clean:
	rm -rf gemm *.o
