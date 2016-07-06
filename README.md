# matrixeQTL2LocusZoom

This script will take three parameters as inputs, 1) Gene ID from ENSEMBL annotation, 2) chromosome number where the gene is located 3) eQTL file from matrixeQTL in the following format:

<pre>
head AOR_TCF21_eqtls.txt
"snps"	"gene"	"statistic"	"pvalue"	"FDR"	"beta"
"6:134214525"	"ENSG00000118526.6"	-8.00604105843143	8.03916943247416e-15	8.27596273928866e-13	-0.472596606956573
"6:134226147"	"ENSG00000118526.6"	-7.76939299996685	4.35609034489325e-14	4.1908757955211e-12	-0.453463080643677
"6:134209837"	"ENSG00000118526.6"	-5.91258104036461	6.16525172030328e-09	3.6491797333611e-07	-0.434239358522576
"6:134215779"	"ENSG00000118526.6"	-5.4626188984354	7.33863755697273e-08	3.7776937355882e-06	-0.335590058154907
"6:134215155"	"ENSG00000118526.6"	-5.46040034813125	7.42581108817843e-08	3.82004547528766e-06	-0.335842843000443
"6:134219229"	"ENSG00000118526.6"	-5.4546658391212	7.6558233417211e-08	3.93297487388231e-06	-0.335279178823917
"6:134204247"	"ENSG00000118526.6"	-5.39357457171944	1.05780776839588e-07	5.3217557036282e-06	-0.397099262828128
"6:134202690"	"ENSG00000118526.6"	-5.37526674283146	1.16474164877705e-07	5.8287500535325e-06	-0.398573998449558
"6:134184272"	"ENSG00000118526.6"	-4.85278383205625	1.61954736331598e-06	6.82414031433209e-05	-0.387056671918765
</pre>

#Executing script
Download matrixeQTL2LocusZoom.sh
Download snp142.cut_tab
<pre>
chmod 755 matrixeQTL2LocusZoom.sh
./matrixeQTL2LocusZoom.sh ENSG00000118526 6 AOR_TCF21_eqtls.txt
</pre>

#Output

Output file will be named according to ENSEMBL geneID and have extension .eQTL.rsIDs, and contain rsIDs and p-values as columns 1 and 2
<pre>
head ENSG00000118526.eQTL.rsIDs
rs3777810 0.395091136884783
rs159417 0.451121029045717
rs74786004 0.486213935779129
rs159418 0.309231443202701
rs73559684 0.653963276491878
rs159419 0.433273033090162
rs149078286 0.176463218466757
rs181411522 0.707869402571322
rs3777811 0.830651265778997
rs34925767 0.761642570067226
</pre>

Plotting in LocusZoom will give (example of cis-eQTLs for TCF21 gene on chromosome 6):

![ScreenShot](
