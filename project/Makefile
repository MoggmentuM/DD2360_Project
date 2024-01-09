#makefile

include make.config

CC := $(CUDA_DIR)/bin/nvcc

INCLUDE := $(CUDA_DIR)/include

all:
    +$(MAKE) -C cuRAND
    +$(MAKE) -C float_stream
    +$(MAKE) -C naive_stream
		+$(MAKE) -C particlefilter_original
    +$(MAKE) -C shared_memory
    +$(MAKE) -C unified_memory

