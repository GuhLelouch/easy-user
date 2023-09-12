# easy-user
 Scripts to facilitate the bulk design of primers for USER cloning and mutagenesis

easy-cloning
This is for when you want to make several plasmids with the same backbone but containing different individual inserts.

How to use:
1. In the file called "template.txt", simply paste the sequence of the template containing the desired backbone.
2. Press Enter and add the position where the inserts will be introduced.
3. Press Enter and add the position where the inserts will end (obs.: anything between the two positions will be deleted, including the bases in these positions)
4. Save the file.
5. In the file named "inserts.fasta", simply add all inserts of interest in the fasta format.
6. Save the file.
7. Run the Python code in a Jupyter notebook.

Requirements:

--------------A--------T-----template-----A--------T--------------
              ^         ^                ^         ^
 6-10 bp from T      insert            insert      6-10 bp from A
                     starts            ends
                     near              near                  
                     here              here
