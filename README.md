## In this fork, a docker image created for weeSAM at: 
```
docker pull alhumaidyaroob/weesam:latest

### to get weeSAM help massage and basic usage: 
docker run --rm alhumaidyaroob/weesam:latest   weeSAM/weeSAM

### Example: 

docker run --rm -v $(pwd):/home/data -w /home/data alhumaidyaroob/weesam:latest   weeSAM/weeSAM --bam sample.bam --out weesam.txt
```


### _weeSAM_  
```  
              _)_
           .-'(/ '-.
          /    `    \
         /  -     -  \
        (`  a     a  `)
         \     ^     /
          '. '---' .'
          .-`'---'`-.
         /           \
        /  / '   ' \  \
      _/  /| S A M |\  \_
     `/|\` |+++++++|`/|\`
          /\       /\
          | `-._.-` |
          \   / \   /
          |_ |   | _|
          | _|   |_ |
          (ooO   Ooo)


``` 

### _usage:_ ### 
``weeSAM { --bam file.bam OR --sam file.sam } --out output.txt `` 


#### _command line options:_   ####  
`--bam` : The input bam file. [file.bam]   
`--sam` : The input sam file. [file.sam]   
`--out` : The name of your output file. [myoutput.txt]     
`--html`: Generate html for each coverage plot produced by the script. [file.html]      
`--overwrite`	: Add this flag to overwrite a html directory from a previous run.
`--mapped`    : Add to generate and analyse a new bam file with only mapped reads.
`-h`    : Print help function.   
`-v`	: weeSAM version number.

#### _File output fields:_  ####  
`Ref_Name` : The identifier of the reference.  
`Ref_Len` : The length in bases of each reference.  
`Mapped_Reads` : Number of reads mapped to each reference.  
`Breadth` : The number of sites in the genome covered by reads.  
`%_Covered` : The percent of sites in the genome which have coverage.  
`Min_Depth` : Minimum read depth observed.  
`Max_Depth` : Max read depth observed.  
`Avg_Depth` : Mean read depth observed.  
`Std_Dev` : Standard deviation of the mean (Avg_Depth).  
`Above_0.2_Depth` : Percentage of sites which have greater than 0.2 * Avg_Depth.  
`Above_1_Depth` : Percentage of sites which are above Avg_Depth.  
`Above_1.8_Depth` : Percentage of sites which have greater than 1.8 * Avg_Depth.  
`Variation_Coefficient` : The mean of Std_Dev of the mean.  


