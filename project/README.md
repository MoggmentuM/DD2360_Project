
To run the code:

Step 1:
git clone https://github.com/MoggmentuM/DD2360_Project.git

Step 2:
make -C /DD2360_Project/project/ (make -C /content/DD2360_Project/project/ for Google Colab).

Step 3:
To run the code, choose which version of the benchmark you want to run.

Original version of ParticleFilter (naive): <br>
./DD2360_Project/project/particlefilter_original/particlefilter_naive -x (input_x) -y (input_y) -z (input_z) -np (input_np)

Original version of ParticleFilter (float): <br>
./DD2360_Project/project/particlefilter_original/particlefilter_float -x (input_x) -y (input_y) -z (input_z) -np (input_np)

Shared memory: <br>
./DD2360_Project/project/Shared_Memory/ex_particle_CUDA_float_seq_SharedMemory -x (input_x) -y (input_y) -z (input_z) -np (input_np)

Unified Memory: <br>
./DD2360_Project/project/Unified_Memory/ex_particle_CUDA_float_seq_SharedMemory -x (input_x) -y (input_y) -z (input_z) -np (input_np)

cuRAND: <br>
./DD2360_Project/project/cuRAND/particlefilter_cuRAND -x (input_x) -y (input_y) -z (input_z) -np (input_np)

Float stream: <br>
./DD2360_Project/project/float_stream/ex_particle_CUDA_float_stream_copy -x (input_x) -y (input_y) -z (input_z) -np (input_np) -nstream (input_nstream)

Naive stream (first version): <br>
./DD2360_Project/project/naive_stream/particlefilter_streams -x (input_x) -y (input_y) -z (input_z) -np (input_np) -nstream (input_nstream)

Naive stream (second version): <br>
./DD2360_Project/project/naive_stream/particlefilter_streams_v2 -x (input_x) -y (input_y) -z (input_z) -np (input_np) -nstream (input_nstream)

Naive stream (bisection version): <br>
./DD2360_Project/project/naive_stream/particlefilter_bisection -x (input_x) -y (input_y) -z (input_z) -np (input_np) -nstream (input_nstream)
