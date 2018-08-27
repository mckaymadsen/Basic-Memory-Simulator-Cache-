# Basic-Memory-Simulator-Cache-

Memory Simulator that functions as a cache. Supports direct mapping, x-way set associativity (2,4,...),
and fully associative Supports LRU and FIFO replacement policies and uses write-back. This code does not include
error checking.

Example input file (input1.txt):

  	4

  	R 0
	
  	W 16
	
  	W 0
	
  	R 8

Example input:


  	Enter the size of main memory in bytes: 128	
  	Enter the size of the cache in bytes: 64	
	Enter the cache block/line size: 8	

  	Enter the degree of set-associativity (input n for an n-way set-associative mapping):n	
  	Enter the replacement policy (L = LRU, F = FIFO): F	
  	Enter the name of the input file containing the list of memory references generated by the CPU: input1.txt
	


Example output:

  	Simulator Output:
	
  	Total address lines required = 7	
  	Number of bits for offset = 3	
  	Number of bits for index = 0	
  	Numbers of bits for tag = 4	
  	Total cache size required = 70.00 bytes	

  	main memory address     mm blk #        cm set #        cm blk #        hit/miss	
                    0            0               1               0            miss								
                   16            2               1               1            miss								 
                    0            0               1               0             hit										
                    8            1               1               2            miss										

  	Highest possible hit rate = 1/4 = 25.00% 	
  	Actual hit rate = 1/4 = 25.00%	

  	Final "status" of the cache:	
	
  	Cache blk #     dirty bit       valid bit       tag     Data	
		0             1               1       0000    mm blk # 0						
		1             1               1       0010    mm blk # 2							
		2             0               1       0001    mm blk # 1						
		3             0               0       xxxx    xxxx						
		4             0               0       xxxx    xxxx						
		5             0               0       xxxx    xxxx						
		6             0               0       xxxx    xxxx						
		7             0               0       xxxx    xxxx						

	Continue? ('y' = yes, any other input = no): n

