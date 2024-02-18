GENCODE_FLAGS =  -gencode arch=compute_80,code=compute_80

gemm: gemm.cu kernel.h
	nvcc $< -o $@ --std=c++11 -O3 $(GENCODE_FLAGS) -Xptxas -v

clean:
	rm -rf gemm *.o