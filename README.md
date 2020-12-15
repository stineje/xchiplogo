# xchiplogo
This is chiplogo a logo generator for VLSI chips.  Originally written by Alireza Moini and modified by yours truly to work on Linux systems.  To get this to work, you have to convert your files to PBM (or Portable Bit Map) format.  To do this, type the following:<BR>
 
<PRE>  
convert -compress none file.jpg file.pbm
</PRE>  

Then, to convert,  you can type:
<PRE>  
xchiplogo file.pbm file.mag
</PRE>

USAGE :
xchiplogo [-c cif_layer_name] [-m magic_layer_name] [-w width] [-s scale] [-t tech_name] [-e] [-v view_array] [-B  threshold_before] [-A threshold_after] input_file [output_file]

The options are: 
 cif_layer_name   => the cif layer name that you like
 magic_layer_name => the magic layer name
 width            => the minimum width of the layer 
 scale            => the scale factor 
 tech_name        => the technology name for magic 
 e                => toggles the error detection and correction option 
 view_factor      => sets the viewing option. 0=NO view, a value greater than or                     equal to one means view with the scaling set at this value 
 threshold_before => the threshold value used in the smoothing before error                          correction (from 4 to 16)
 threshold_after  => the threshold value used in the smoothing after error                          correction (from 4 to 16)
 NOTE: The input file should be in the ascii bit map format

 the defaults are as follows:

          magic_tech_name   = scmos 
          magic_layer_name  = poly 
          minimum_width     = 1
          scale             = 1
          error_correct     = 1
          threshold_before  = 4 (max=16) 
          magic_output_file = logo.mag 
          cif_output_file   = logo.cif 

