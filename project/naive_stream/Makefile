#makefile

include ../make.config

CC := $(CUDA_DIR)/bin/nvcc

INCLUDE := $(CUDA_DIR)/include

all: streams_naive streams_v2 streams_v2_bisetion

streams_naive: ex_particle_streams_naive.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_streams_naive.cu -o particlefilter_streams
	

streams_v2: ex_particle_streams_naive_v2.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_streams_naive_v2.cu -o particlefilter_streams_v2
	
streams_v2_bisetion: ex_particle_streams_naive_bisection.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_streams_naive_bisection.cu -o particlefilter_bisection

clean:
	rm particlefilter_bisection particlefilter_streams particlefilter_streams_v2
