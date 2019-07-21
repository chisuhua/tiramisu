The files in this folder are organized as follows:

    General
        clean.sh : remove some useless files.
        compile_and_run_mkl.sh : compile MKL code and run it. 
        configure.h: define some configuration constants.

    Tiramisu
        resize_conv_generator_tiramisu.cpp: Tiramisu code generator.

    Wrapper
        wrapper_nn_block.cpp: wrapper file that calls the code generated by Tiramisu.

    Intel MKL
        resize_conv_generator_mkl.c: code that calls Intel MKL. 

To run this benchmark:

    At the directory build/benchmarks/DNN/blocks/Resize-Conv execute 
	    make 

    wrapper_nn_block_resize_conv executable will be created in the current directory. 
    
    To compare the result of tiramisu with MKL execute :
        ./compile_and_run_mkl.sh
    then 
        ./wrapper_nn_block_resize_conv
    
    execution results could be found in the text files : 
        mkl_result.txt
        tiramisu_result.txt