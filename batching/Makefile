CUDA_PATH = /sw/spack/deltas11-2023-03/apps/linux-rhel8-zen/gcc-8.5.0/cuda-12.2.1-t7b4feq
CUDNN_PATH = /sw/external/libraries/cudnn-linux-x86_64-8.9.0.131_cuda11-archive
GENCODE_FLAGS =  -gencode arch=compute_80,code=compute_80

gemm: gemm.cu kernel.h
	nvcc $< -o $@ --std=c++11 -O3 $(GENCODE_FLAGS) -I$(CUDA_PATH)/include -I$(CUDNN_PATH)/include -L$(CUDA_PATH)/lib64 -L$(CUDNN_PATH)/lib -lcudnn -Xptxas -v -res-usage

clean:
	rm -rf gemm *.o
