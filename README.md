# FTRACE_for_kernel
Enable FTRACE for Kernel

 How to enable Ftrace for kernel?

 1)
 > make kernel_menuconfig

 2)
 Enable the below configs.

 CONFIG_FTRACE=y
 
 CONFIG_DYNAMIC_FTRACE=y
 
 CONFIG_FUNCTION_TRACER=y
 
 CONFIG_STACK_TRACER

 3)
 Compile kernel

 4)
   echo function_graph > /sys/kernel/debug/tracing/current_tracer

   echo 1 > /sys/kernel/debug/tracing/tracing_on

   echo 0 > /sys/kernel/debug/tracing/tracing_on

 6) View the logs:
    
 cat  /sys/kernel/debug/tracing/trace

 7) Clear the logs
    
 echo >  /sys/kernel/debug/tracing/trace





