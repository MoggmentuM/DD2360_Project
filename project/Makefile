include make.config

CC := $(CUDA_DIR)/bin/nvcc
INCLUDE := $(CUDA_DIR)/include

SUBDIRS := cuRAND float_stream naive_stream particlefilter_original Shared_Memory Unified_Memory

.PHONY: all $(SUBDIRS)

all: $(SUBDIRS)

$(SUBDIRS):
	@echo "Making in $@"
	$(MAKE) -C $@