#makefile

include make.config

CC := $(CUDA_DIR)/bin/nvcc

INCLUDE := $(CUDA_DIR)/include

all: float_stream

streams: ex_particle_CUDA_float_stream.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_CUDA_float_stream.cu -o particlefilter_streams
	
#cuRAND: ex_particle_cuRAND_float_seq.cu
#	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_cuRAND_float_seq.cu -o particlefilter_cuRAND

#streams_v2: ex_particle_streams_naive_bisection.cu
	#$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_streams_naive_bisection.cu -o particlefilter_bisection

clean:
	rm particlefilter_streams
