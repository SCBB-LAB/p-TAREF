Readme First 


p-TAREF: A fast and accurate tool to Refine plant microRNA Target Prediction

please visit http://scbb.ihbt.res.in/ 

1.System Requirement
2.Installation
3.p-TAREF execution
4.File formats


1.System requirement:

Linux O.S. (Ubuntu)
Vienna RNA package
EMBOSS (# sudo apt-get install emboss -y)
RNAhybrid (# sudo apt-get install rnahybrid -y)
libSVM (# sudo apt-get install libsvm* -y)

2.Installing:

Extract p-TAREF on your local system migrate to Dependencies directory and as root execute ./install toinstall all dependencies required by p-TAREF.


3.p-TAREF execution:

 To run p-TAREF from command line: 
sh run.sh <mRNA file> <energy cutoff> <mismatch allowed> <kernel "p" for polynomial kernel, "g" for gaussian kernel and "l" for linear kernel> <result folder> <all> <number of processors>
 
 
 <mRNA file>    mRNA sequence(s) in FASTA format.
 <energy cutoff>	minimum free energy of miRNA-target duplex
 <mismatch allowed>	maximum mismatch allowed
 <kernel>	Choose between three kernels (most stringent polynomial, moderate stringent gaussian and least stringent linear)
 <result folder>	specify the result folder. defaul folder is same folder which contains input file
 <all> or <same>	scan predicted miRNA with all encoded patterns/scan predicted miRNA with same miRNA encoded patterns
 <Number of processos>	Number of processors on which you want to execute p-TAREF



4.File formats:

# Sequence should be in fasta format followed by TAIR ID.
# Sequences can be in multiple line or in single line.

>AT1G02860.1
ATGTTCCCAAAACAAACGTTTTGACTTTTTTTTTGTTTTCTCATATTCTTTTATTTCACAACTTGTTATTTCCGCCGACTTCACCAGTCACCACCACCTT
CATTTATTCATAAATACGTCTCTGTTCTGTTTTTGTTTCTGTTTCATTTTCATACATAATTAAGCCAACACGAGACGCAAGAGAGAGATAGGGAAAGAGA



Use >ATXXXXXX format for any query

Please put "AT" followed by some accession number to create imaginary ID to fit the format requirement: for example if the accession id is ">Os01g04550" change it to something like ">AT01g04550"
OR you can create any imaginery ID with >ATXXX format to meet the input requirement.




For query, bugs or information please contact ravish@ihbt.res.in or sg927357@gmail.com or log on to scbb.ihbt.res.in
  
Citation: Jha, A., Shankar, R. Employing machine learning for reliable miRNA target identification in plants. BMC Genomics 12, 636 (2011). https://doi.org/10.1186/1471-2164-12-636
