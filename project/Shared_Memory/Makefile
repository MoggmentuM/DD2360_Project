#makefile

include ../make.config

CC := $(CUDA_DIR)/bin/nvcc

INCLUDE := $(CUDA_DIR)/include

all: shared

shared: ex_particle_CUDA_float_seq_SharedMemory.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_CUDA_float_seq_SharedMemory.cu -o ex_particle_CUDA_float_seq_SharedMemory
	
clean:
	rm ex_particle_CUDA_float_seq_SharedMemory