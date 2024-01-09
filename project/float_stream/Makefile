#makefile

include ../make.config

CC := $(CUDA_DIR)/bin/nvcc

INCLUDE := $(CUDA_DIR)/include

all: float_stream float_stream_v1

float_stream: ex_particle_CUDA_float_stream.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_CUDA_float_stream.cu -o ex_particle_CUDA_float_stream

float_stream_v1: ex_particle_CUDA_float_stream_copy.cu
		$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_CUDA_float_stream_copy.cu -o ex_particle_CUDA_float_stream_copy

clean:
	rm ex_particle_CUDA_float_stream ex_particle_CUDA_float_stream_copy
