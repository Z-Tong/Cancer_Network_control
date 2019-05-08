# Instruction of Cancer_Network_control package
%Remainder: Please install gurobi before running our code (http://www.gurobi.com/)
%Remainder: Please install gurobi before running our code (http://www.gurobi.com/)
%Remainder: Please install gurobi before running our code (http://www.gurobi.com/)
This package includes Matlab scripts and several datasets for demo of cancer_network_control approaches:
(a)	main_cancer_network_control.m is a Matlab function for the routine of experimental analysis.
(b)	 main_cancer_network_control.m is the main script to call cancer_network_control by supplying following parameters:
    (1)	expression_tumor_fileName: the directory locating of the gene tumor expression data as the input data.
    (2)	expression_normal_fileName: the directory locating of the gene normal expression data as the input data.
(b)  cancer_network_control.m is the main script to call cancer_network_control
(c)  The input datasets include:
    (1) expression_tumor_fileName.txt: the gene tumor expression data.
    (2) expression_normal_fileName.txt: the gene normal expression data.
        Note that the samples in expression_tumor_fileName.txt  and expression_normal_fileName.txt  should be paired.
     (3) index: denotes we use which network construction method 
         %if index=1,we use SSN [1].
         %if index=2,we use paired SSN [2].
         %if index=3,we use LIONESS [3].

The output datasets include:
The sample-specific driver profiles (matrix) by using MMS[4],MDS[5],DFVS[6],NCUA[2]；
For “MMS or MDS,DFVS,NCUA”, the column is the samples and the rows is the genes. The value “1” denoted that the gene is driver genes; 
(d) As a demo, users can directly run main_Benchmark_control.m in Matlab. We choose the BRCA cancer data as a test case in our demo. This package has been tested in different computer environments as: Window 7 or above; Matlab 2014 or above.
(e) When users analyzed yourself new data, please:
   (1) Prepare input datasets as introduced in (d).
   (2) Clear the previous results.
   (3) Set parameters in benchmark_control.m as introduced in (b).
   (4) Run main_Benchmark_control.m.
   (5) Suggest that the users add all fille in our folders to your folder.

%   $Id: main_Benchmark_control.m Created at 2019-05-08 18:15:16 $
%   by Weifeng Guo, Northwestern Polytechtical University, China
%   Copyright (c) 2014-2019 by Key Laboratory of Information Fusion Technology of Ministry of Education in Northwestern Polytechnical University,
%   and key Laboratory of Systems Biology in Shanghai Institutes for Biological Science; 
%   If any problem,pleasse contact shaonianweifeng@126.com for help.

References
[1] Liu X, Wang Y, Ji H et al. Personalized characterization of diseases using sample-specific networks, Nucleic Acids Research 2016;44:e164-e164.
[2] Guo W-F, Zhang S-W, Zeng T et al.Controlling the large scale biological networks with a novel structure control method, bioRxiv 2019:503565.
[3] Kuijjer ML, Tung M, Yuan G et al. Estimating sample-specific regulatory networks, ISCIENCE 2019, doi: 10.1016/j.isci.2019.03.021.
[4] Liu Y Y, Slotine J J, Barabási A L. Controllability of complex networks[J]. nature, 2011, 473(7346): 167.
[5] Nacher JC, Akutsu T. Dominating scale-free networks with variable scaling exponent: heterogeneous networks are not difficult to control, New Journal of Physics 2012;14:73005-73028(73024).
[6] .Jgt Z, Yang G, Albert R. Structure-based control of complex networks with nonlinear dynamics, Proceedings of the National Academy of Sciences of the United States of America 2017:7234-7239.

