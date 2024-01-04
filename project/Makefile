#makefile

include make.config

CC := $(CUDA_DIR)/bin/nvcc

INCLUDE := $(CUDA_DIR)/include

all: streams tpb tpb_float

tpb: ex_particle_naive_tpb.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_naive_tpb.cu -o particlefilter_tpb

tpb_float: ex_particle_float_tpb.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_float_tpb.cu -o particlefilter_tpb_float

streams: ex_particle_streams_naive.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_streams_naive.cu -o particlefilter_streams
	
#cuRAND: ex_particle_cuRAND_float_seq.cu
#	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_cuRAND_float_seq.cu -o particlefilter_cuRAND

#streams_v2: ex_particle_streams_naive_copy.cu
#	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math -arch sm_75 ex_particle_streams_naive_copy.cu -o particlefilter_streams_v2

clean:
	rm particlefilter_streams tpb tpb_float
