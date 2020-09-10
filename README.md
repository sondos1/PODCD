# PODCD
source code of PODCD: probablistic overlapping dynamic community detection
‎========================================================================‎
‎    PODCD: probabilistic overlapping dynamic community detection.‎
‎========================================================================‎
The example implements a large scale overlapping community detection method based on Cluster ‎Affiliation Graph Model for Big Networks (PODCD).‎
This program formulates community detection problems into non-negative matrix factorization and ‎discovers community membership factors of nodes by maximum likelihood estimation. User can ‎specify how many communities she would detect, or let the program determine the number of ‎communities in the network from the topology of the network.‎
Fitting procedure and the community-Affiliation Graph Model are described in the following paper:‎
Sondos Bahadori, Hadi Zare, Parham Moradi, “PODCD: Probabilistic Overlapping Dynamic Community ‎Detection”‎

The code works under Windows with Visual Studio or Cygwin with GCC, Mac OS X, Linux and other ‎Unix variants with GCC. Make sure that a C++ compiler is installed on the system. Visual Studio project ‎files and makefiles are provided. For makefiles, compile the code with
‎"make all".‎

‎/////////////////////////////////////////////////////////////////////////////‎
Parameters:‎
‎   -o:Output Graph data prefix (default:'')‎
‎   -i:Input edgelist file name (default:'../g’)‎
‎   -l:Input file name for node names (Node ID, Node label)  (default:'')‎
If we want to specify the number of communities in each snapshot ourselves, we should change the ‎values of cc[] array in bigclam.cpp code so that it contains number of communities in each snapshot, ‎for example if we have three snapshot , that number of communities in order are 16,17and 15 , then ‎the values of cc[] array be as :cc[]={16,17,15}. If we want the program detect number of communities ‎we should set the values of the following parameter as -1 else the value of this parameter set to ‎another value except -1 and initialize cc[] as describe before. ‎
‎   -c:The number of communities to detect (-1: detect automatically) .‎
‎   The following three parameters are for finding the number of communities to detect.‎
‎   The program tries nc numbers from mc to xc: by default, it tries 10 values from 5 to 100.‎
‎   -mc:Minimum number of communities to try (default:5) ‎
‎   -xc:Maximum number of communities to try (default:100)‎
‎   -nc:How many trials for the number of communities (default:10)‎
‎      -nt:Number of threads for parallelization (default:1) -nt:1 means no parallelization.‎
‎      The following two parameters are for backtracking line search described in Convex Optimization, ‎Boyd and Vandenberghe, 2004.‎
‎   Refer to the book for the backtracking line search algorithm.‎
‎   -sa:Alpha for backtracking line search (default:0.3)‎
‎   -sb:Beta for backtracking line search (default:0.3)‎
The following parameters defne number o snapshots:‎
‎-Tm: number of snapshots.‎
‎/////////////////////////////////////////////////////////////////////////////‎
‎**As input file we need two type file. The first ones are edge files and rhe second ones are files tha ‎their name is as “nodeT”, that T is the number of snapshots. For example g2.txt contains edges file in ‎‎2-snapshots and node2 file contains list of presenting nodes in g2.txt in the order they have ‎presented.‎
‎/////////////////////////////////////‎
‎ ‎
The path of opening the program in visual studio is as following:‎
Podce->examples->podcd->podcd.SLN‎
‎/////////////‎
‎** for the simplicity of usage it is better to copy the input files in the following path:‎
Podce->examples->bigclam‎
‎///////////////‎
Some ample networks presented in the following path:‎
Podce->sample networks‎
All the sample networks generated using Greene’s benchmark. All the sample networks have 10 ‎snapshots. Each folder in sample networks folder contain 3 sample foe each type of network ‎evolution.‎
Each sample network folder contains three type files:‎
g1-10.txt: edges files.‎
node1-10: contain nodes in order presented in edges files.‎
One1-10: ground truth of network in each snapshot.‎
If the user want run the program on each of this sample networks, step of works to do is as following:‎
‎1- Copy g1-10.txt and node1-10 to the following folder:‎
Podce->examples->bigclam‎
‎2- If the user want to specify the number of communities, the user should specify the value of cc[] ‎array . The correct number of communities in each snapshot is the number of lines in one1-10.txt files ‎that each line of this files is a ground truth communities.‎
‎//////////////////////////////////////////////‎
To ask any question you can send an email to sondos_bahadori@yahoo.com


