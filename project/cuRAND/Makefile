#makefile

include ../make.config

CC := $(CUDA_DIR)/bin/nvcc

INCLUDE := $(CUDA_DIR)/include

all: cuRAND

cuRAND: ex_particle_cuRAND_float_seq.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_cuRAND_float_seq.cu -o particlefilter_cuRAND

clean:
	rm particlefilter_cuRAND
