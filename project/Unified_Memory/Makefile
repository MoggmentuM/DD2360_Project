#makefile

include ../make.config

CC := $(CUDA_DIR)/bin/nvcc

INCLUDE := $(CUDA_DIR)/include

all: unified_memory_float unified_memory_naive

unified_memory_float: ex_particle_CUDA_float_seq_UnifiedMemory.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_CUDA_float_seq_UnifiedMemory.cu -o ex_particle_CUDA_float_seq_UnifiedMemory
	
unified_memory_naive: ex_particle_CUDA_naive_seq_UnifiedMemory.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_CUDA_naive_seq_UnifiedMemory.cu -o ex_particle_CUDA_naive_seq_UnifiedMemory

clean:
	rm ex_particle_CUDA_float_seq_UnifiedMemory ex_particle_CUDA_naive_seq_UnifiedMemory