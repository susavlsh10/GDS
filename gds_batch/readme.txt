This repo consist of GPUDirect kernels with batch submissions 

cufile_bread.cc : This file submits multiple batches in a for loop. 
./cufile_bread float_4194304_a.dat 0 128 8 1

cu_bread.cc: This file submits multiple batches using threads.
./cu_bread float_4194304_a.dat 0 128 8 1 

// The command above selects GPU 0 for GDS reads, 128 io in the batch and 8 batches. The last argument is used to scale the io size in multiple of 4KB. In this example, we use 4096*1 = 4096 bytes per io. 

