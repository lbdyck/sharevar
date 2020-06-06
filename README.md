# sharevar
Share REXX Variables, and stems, between REXX Execs

SHAREVAR is a REXX program designed to make it easy to share REXX               
variables, including stems, between different REXX programs.  Only stems        
that are numeric,and for which stem.0 has the count, are supported.             
                                                                                
All listed variables, including stem variables will be encoded into             
the ISPF variable that is then saved in the ISPF Shared variable Pool           
with a Put and all variables in the list will be reconstituted on the           
Get.                                                                            
                                                                                
Examples are provided:                                                          
                                                                                
          TVX is the driver demonstration exec. Invoke it with a dataset        
          name, or let it default to SYS1.PARMLIB, and it invokes TVX0          
          to create a set of REXX variables and a stem. The variables           
          are then 'put' to an ISPF variable of 'dsi'. Next TVX invokes         
          TVX1 to 'get' the 'dsi' variable, decodes it to recreate all          
          of the original variables, including the stem. TVX1 then              
          displays, using the say instruction, the variables and their          
          values.      
