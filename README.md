# FASTA-colours
A tool that creates an R colour palette from the counted base pairs of a given FASTA file. Use-cases include when you're a nerd about graphs and figures, or when you've run out of anything else to say about your poster.  
  
## How it works  
Since bases G and T are outside the hexadecimal colour range (0-9 and A-F), they are converted to the nearest accepted alphabetical characaters. Therefore, G becomes D and T becomes E. Base pair counts are truncated so that only the first digit is kept. The converted base pair counts are then cycled to create 4 hexadecimal colour codes, outputted to a CSV.   

## Example I/O  
Pass import_fasta.py a FASTA file.  
  
Counted base pairs:  
A = 1224, C = 6212, G = 782, T = 2825  
  
Output:  
1A6C7D  
6C7D2E  
7D2E1A  
2E1A6C  
  
See example_palette.R for how one might import the output CSV and use the colours for plotting.  
