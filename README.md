# 1. easy-user
Scripts to facilitate the bulk design of primers for USER cloning and mutagenesis

simple-cloning:
This is for when you want to make several plasmids with the same backbone but containing different individual inserts.

simple-mutagenesis:
This script can used to make several plasmids with the same backbone and gene but different single-point mutations. Useful for screening any size of libraries of rationally designed single-point variants. Can be potentially used to simultaneously make multi-point mutations separated by ~60 bases.

any-mutagenesis (future idea):
This will be used to produce any desired mutations in a single region of a plasmid codifying for a protein, including multi-point mutations, deletions, insertions, and a combination of all of those.

# 2. Dependencies
If not already installed in the appropriate environment, please install pandas library with:
pip install pandas

The same is valid for the Biopython library:
pip install biopython

# 3. Scripts
# 3.1. simple-cloning
# 3.1.1. How to use simple-cloning
1. In the file called "template.txt", simply paste the sequence of the template containing the desired backbone.
2. Press Enter and add the position where the inserts will be introduced.
3. Press Enter and add the position where the inserts will end (obs.: anything between the two positions will be deleted, including the bases in these positions)
4. Save the file.
5. In the file named "inserts.fasta", simply add all inserts of interest in the fasta format.
6. Save the file.
7. Run the Python code in a Jupyter notebook.

Output:
The output is an Excel file named "primers_list.xlsx". There you can find the resulting primers.

Requirements:

--------------A--------T-----template-----A--------T--------------
              ^         ^                ^         ^
 6-10 bp from T      insert            insert      6-10 bp from A
                     starts            ends
                     near              near                  
                     here              here

# 3.1.2. Notice
It is very likely that many inserts will share the same backbone primers. However, the script doesn't delete those redundancies yet. Therefore, be careful not to send the same primers several times for synthesis.

# 3.2. simple-mutagenesis
# 3.2.1. How to use simple-mutagenesis
1. In the file called "plasmid.txt", simply paste the sequence of the plasmid containing the gene where the mutations are to be made.
2. Press Enter and write the position where the gene starts.
3. Press Enter and write the position where the gene ends.
4. Press Enter and paste the sequence of the gene.
5. Save the file.
6. In the file named "mutations.txt", simply write all mutations of interest in different lines. (use the one-letter format for amino acids)
7. Save the file.
8. Run the Python code in a Jupyter notebook.

Output:
The output is an Excel file named "primers_list.xlsx". There you can find the resulting primers.
