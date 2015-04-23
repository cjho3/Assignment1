# BLAST, orthologs, and paralogs (Week 2, 20 pts possible)

__Name:__ Chadwick Ho

__Student ID:__ 998510369

*_Please answer the following questions which are each worth 2 points. Be clear and concise with any written answers. Late assignments will be penalized with a 2pt deduction without prior communication of extenuating circumstances._*

__Q1__.  Paste in code and output for the `for loop`  __Exercise 1__ (pluralizing fruit names)

	bis180lstudent@bis180lstudent-VirtualBox:~/BIS180L_Assignments_Chadwick.Ho/Assignment_2$ vegetables="peach tomato potato"
	bis180lstudent@bis180lstudent-VirtualBox:~/BIS180L_Assignments_Chadwick.Ho/Assignment_2$ echo "$vegetables"
	peach tomato potato
	bis180lstudent@bis180lstudent-VirtualBox:~/BIS180L_Assignments_Chadwick.Ho/Assignment_2$ for vegetable in $vegetables
	> do
	> echo "${vegetable}es"
	> done
	peaches
	tomatoes


__Q2__. Create a table that indicates blastp runtime as a function of word size.  Is there a linear relationship?  Why does does changing the word size change the search time?

|word length| blastp runtime
|:---------------|:--------------------
| 1 		| 27.309s
|2		| 4.012s
|3		| 0.877s
|4		| 0.301s
|5		| 0.167s
|6		| 0.155s

The relationship is not a linear relationship, but an exponential decay. Changing the word size drastically decreases the number of possible matches. It changes the parameters of search and thus changes the sensitivity.

__Q3__.  How much faster is blastp than water at a world size of 5?

It is about 10 times faster at word size of 5.

__Q4__.  How long will it take to search two proteomes with word length 5?

It will take about fifty minutes to an hour to search two proteoms with word length 5.

__Q5__.  Using E-value to determine the best match, find a worm gene with a single fly ortholog and record their names and the reciprocal E-Values.  Is there more than one fly "hit" for your worm gene?  If so how do you decide if there is a single orthlog?

Fly gene: FBpp0079278
Worm gene: ZK742.1a		
E-value: 6.1e-288

No, there was only one hit for worm gene ZK742.1a, the fly gene FBpp0079278. I used "grep" to sift through to find a worm gene that had a single fly ortholog.

__Q6__.  What logic would you use to find orthologs automatically using BLAST?

When looking for orthologs in BLAST, it can be automatically assumed as an ortholog if a gene is a 1 to 1 match with another protein after reciprocal BLASTing. It also has to be taken into account that the two proteins that are matched cannot have too high of a percent identity, which could imply duplication, so a parameter needs to be in place when testing.

__Q7__.  Discuss what makes orthology difficult to determine by the reciprocal BLAST method.

Orthology is difficult to determine because in reciprocal BLAST  it only takes into account the best pairs based on E-value. This is difficult to determine when looking at the matches, and finding that a protein may also match to others within the same genome (i.e 1 protein matches to multiple).

__Q8__.  How many paralogs did you find for T21B10.2a and for B0213.10?  What criteria did you use?

For T21B10.2a I found 6 paralogs, and for B0213.10 I found 4 paralogs. I ran a reciprocal blast, and searched using "grep" to find matches in both. I took the E-value into account, as well as the percent identity. 

__Q9__.  Discuss what makes paralogy difficult to determine by BLAST.

Paralogy was difficult to determine because I was not sure if the percent identity was high enough to consider certain matches as being paralogous. Also, it is difficult if the E-value is not low enough to signify that the match is not by random chance.

__Q10__.  Is alignment score sufficient for determining orthology or paralogy? What other sources of information from the BLAST output might be useful?  What other types of analyses would be helpful?

Alignment score is sufficient for determining orthology because it indicates that the higher the score, the more similar to sequences are to each to other. Orthologous genes are closer related than paralogous genes because they occured through speciation rather than a duplication event. Percent identity and alignment length could be useful tools to use together. Together they can tell us if the length of the alignment is significant and whether the percent identity should be a useful tool as well. The percent identity can tell us how similar two genes are to each other, based on the sequence alignment, and if it is significant, could be an indicator of orthology or paralogy. It would be helpful to find orthology or paralogy through phylogenetic analyses or  experiments. 

Add and commit changes for both this document and your lab notebook to the repository.  Push to GitHub and set an issue to indicate that you are ready for this to be graded.