
To run the code:

Step 1:
git clone https://github.com/MoggmentuM/DD2360_Project.git

Step 2:
make -C /DD2360_Project/project/ (make -C /content/DD2360_Project/project/ for Google Colab).

Step 3:
To run the code, choose which version of the benchmark you want to run. the input arguments to write a number are written as follows: <input>

Original version of ParticleFilter (naive): ./DD2360_Project/project/particlefilter_original/particlefilter_naive -x <x> -y <y> -z <z> -np <np> 

Original version of ParticleFilter (float): ./DD2360_Project/project/particlefilter_original/particlefilter_float -x <x> -y <y> -z <z> -np <np>

Shared memory: ./DD2360_Project/project/Shared_Memory/ex_particle_CUDA_float_seq_SharedMemory -x <x> -y <y> -z <z> -np <np>

Unified Memory: ./DD2360_Project/project/Unified_Memory/ex_particle_CUDA_float_seq_SharedMemory -x <x> -y <y> -z <z> -np <np>

cuRAND: ./DD2360_Project/project/cuRAND/particlefilter_cuRAND -x <x> -y <y> -z <z> -np <np>

Float stream: ./DD2360_Project/project/float_stream/ex_particle_CUDA_float_stream_copy -x <x> -y <y> -z <z> -np <np> -nstream <nstream>

Naive stream (first version):./DD2360_Project/project/naive_stream/particlefilter_streams -x <x> -y <y> -z <z> -np <np> -nstream <nstream>

Naive stream (second version): ./DD2360_Project/project/naive_stream/particlefilter_streams_v2 -x <x> -y <y> -z <z> -np <np> -nstream <nstream>

Naive stream (which uses bisection ./DD2360_Project/project/naive_stream/particlefilter_bisection  -x <x> -y <y> -z <z> -np <np> -nstream <nstream>
