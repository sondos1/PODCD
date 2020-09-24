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

‎   -i:Input edgelist file name (default:'../g’)‎

‎   -c:The number of communities to detect (-1: detect automatically) .‎

‎      -nt:Number of threads for parallelization (default:1) -nt:1 means no parallelization.‎

‎-Tm: number of snapshots.‎

‎/////////////////////////////////////////////////////////////////////////////‎


The path of opening the program in visual studio is as following:‎

Podce->examples->podcd->podcd.SLN‎

‎///////////////////////////////////////////////////////////////////‎


Some ample networks presented in the following path:‎
Podce->sample networks‎

‎//////////////////////////////////////////////‎

To ask any question you can send an email to sondos_bahadori@yahoo.com


