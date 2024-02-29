## Objetivo
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static)? This [BASH script](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh) might help!!

## Solución
```
jars-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
--2024-02-27 18:49:04--  https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
8#TT 1tt$DN'static'
 @@ 0@)pp V``^okyjars-picoctf@webshell:~$ 
static                                                     100%[=======================================================================================================================================>]   8.18K  --.-KB/s    in 0s      

2024-02-27 18:49:04 (139 MB/s) - 'static' saved [8376/8376]

jars-picoctf@webshell:~$ ls
README.txt  flag  static  warm
jars-picoctf@webshell:~$ cat static 
 HH/lib64/ld-linux-x86-64.so.2GNUGNU'}3ZfB
                                          = 
       H                                    Y h "libc.so.6puts__cxa_finalize__libc_start_mainGLIBC_2.2.5_ITM_deregisterTMCloneTable__gmon_start___ITM_registerTMCloneTableui    1
 Ht5
 %
 @%
 h%
H=1I^HHPTLH
 DH=
 UH
 H9HtHZ
]f.]@f.H=
 H5
 UH)HHHH?HHtH!
 Ht
   ]f]@f.=I
 u/H=    UHt
H!          H=   
 ]fDUH]fUHH=]f.DAWAVIAUATL%F UH-F SAIL)HWHt 1LLDAHH9u[]A\A]A^A_Ðf.Oh hai! Wait what? A flag? Yes, it's around here somewhere!8
                                                                                                                              T<,zRx
                                                                                                                                   Rx
                                                                                                                                     FJ
R                                                                                                                                      ?;*3$"D\JAC
D|PeBBE B(H0H8M@r8A0A(B BBx0
o`

 picoCTF{d15a5m_t34s3r_f5aeda17}GCC: (Ubuntu 7.5.0-3ubuntu1~18.04) 7.5.08Tt`


   @ 
 $  k  1C@ Ji v `eH o0+@ :@     "
                                 crtstuff.cderegister_tm_clones__do_global_dtors_auxcompleted.7698__do_global_dtors_aux_fini_array_entryframe_dummy__frame_dummy_init_array_entrystatic.c__FRAME_END____init_array_end_DYNAMIC__init_array_start__GNU_EH_FRAME_HDR_GLOBAL_OFFSET_TABLE___libc_csu_fini_ITM_deregisterTMCloneTableputs@@GLIBC_2.2.5_edata__libc_start_main@@GLIBC_2.2.5__data_start__gmon_start____dso_handle_IO_stdin_used__libc_csu_init__bss_startmain__TMC_END___ITM_registerTMCloneTableflag__cxa_finalize@@GLIBC_2.2.5.symtab.strtab.shstrtab.interp.note.ABI-tag.note.gnu.build-id.gnu.hash.dynsym.dynstr.gnu.version.gnu.version_r.rela.dyn.rela.plt.init.plt.got.text.fini.rodata.eh_frame_hdr.eh_frame.init_array.fini_array.dynamic.data.bss.comment
```
## Notas adicionales
## Referencias 