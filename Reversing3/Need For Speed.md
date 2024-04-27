## Objetivo
The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/f9abc386dfb1309e687344783f208b20/need-for-speed).
## Solución
```
End of assembler dump.
(gdb) call (int) get_
get_avphys_pages                  get_common_indices[constprop]     get_kernel_syms                   get_mnt_entry                     get_nproc_stat                    get_scope
get_common_cache_info             get_current_dir_name              get_kernel_syms@GLIBC_2.2.5       get_myaddress                     get_nprocs                        get_subexp_sub
get_common_cache_info[constprop]  get_function                      get_key                           get_myaddress@GLIBC_2.2.5         get_nprocs_conf                   
get_common_indices                get_input_bytes                   get_locked_global                 get_next_alias                    get_phys_pages                    
(gdb) call (int) get_ke
get_kernel_syms              get_kernel_syms@GLIBC_2.2.5  get_key                      
(gdb) call (int) get_key()
Creating key...
Finished
$2 = 9
(gdb) call (int) print_flag()
Printing flag:
PICOCTF{Good job keeping bus #190ca38b speeding along!}
$3 = 56
(gdb) 

```
## Notas adicionales
## Referencias 