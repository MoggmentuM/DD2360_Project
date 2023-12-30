#makefile

include make.config

CC := $(CUDA_DIR)/bin/nvcc

INCLUDE := $(CUDA_DIR)/include

all: streams streams_v2

streams: ex_particle_streams_naive.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_streams_naive.cu -o particlefilter_streams
	
#cuRAND: ex_particle_cuRAND_float_seq.cu
#	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_cuRAND_float_seq.cu -o particlefilter_cuRAND

streams_v2: ex_particle_streams_naive_v2.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_streams_naive_copy.cu -o particlefilter_streams_v2

clean:
	rm particlefilter_streams particlefilter_streams_v2
