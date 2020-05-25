# What can we learn from a DNA sequence?
During our last metagenomic sequencing expedition in the Pacific Ocean, we retrieved an unknown sequence (contig_unknown.fasta).

What can we learn from this unknown DNA sequence?

## Who is there?
The first question that comes in mind when dealing with an unknown sequence is trying to identify the "who"?

Along the years, scientists have collected a large collection of genomes from a broad number of organisms. 
One of these database is maintained by the National Center for Biotechnology Information (NCBI), and is called GenBank. 
Ressource: [GenBank](https://www.ncbi.nlm.nih.gov/genbank/)

We first want to compare our sequence to this large ressource. To do so, we will use a very very (very) famous algorithm: Blast.

### BlastN query
Go to the [NCBI Blast page](https://blast.ncbi.nlm.nih.gov/Blast.cgi) and select the Nucleotide Blast tool.

Paste the sequence in the "Enter Query Sequence" imput box and choose the "Nucleotide collection (nr/nt)" datasbase to query. Run the algorithm to identify "Highly similar sequences (megablast)".

** Q1: Look at the results. What can we say about the sequence? What type of organism is it? **

** Q2: What is a phage? What kind of organism does it infects? **

Ressources: [MicrobeWiki](https://microbewiki.kenyon.edu/index.php/MicrobeWiki)

## What is it doing ?

Next we want to get an idea of what information we can retrieve on the functions carried in this DNA sequence. 

** Q3: What is a gene? How can we identify a gene in a DNA sequence? **

### Heuristic ORF finder

To retrieve the ORFs from our sequence, we'll use the heuristic [GeneMark](http://opal.biology.gatech.edu/GeneMark/heuristic_gmhmmp.cgi).

Paste the sequence in the input box. Select "Protein sequence" as output. Leave the other parameters as default. Run GeneMark and open the protein sequence output.

** Q4: How many ORFs did the algoritm identify in our sequence? **

## BlastP

In order to get a clue about the functions of these proteins, we can use [BlastP](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PAGE=Proteins) against the NCBI protein database.

Paste our protein sequences (unknown_proteins.fasta) in the input query box, and choose to run BlastP against the "Reference proteins (RefSeq_protein)" database. Leave the other parameters as default and run BlastP.

Browse the results for each of the putative proteins.

** Q5: What type of functions did we identify? Is it surprising? **

Let's look closely at the protein nb4 'gene_4|GeneMark.hmm|341_aa|+|9466|10491'. Select the Top 10 hits for this protein and look at the result as a "Distance tree".

** Q6: In what type of organism do we find this protein? What do you think happened here?**

## Where can we find it ?

Finally, we want to explore the distribution and abundance of this gene in ecosystems. To do so we'll use the [Ocean Gene Atlas](http://tara-oceans.mio.osupytheas.fr/ocean-gene-atlas/).

Using the 'gene_4|GeneMark.hmm|341_aa|+|9466|10491' as input, query the "OM-RGCv1 - Tara Ocean Microbiome" database. Set the "Expect threshold" to 1e-200.

** Q7: Where this gene can be found in the ocean? Rather at the surface or deep in the sea ? Does that make sense from what we know about this gene ?**





