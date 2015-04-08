# Template for Sequence Alignment Assignment (Week 1, 20 pts possible)

__Full Name:__ Chadwick Ho

__Student ID:__ 998510369

*_Please answer the following questions which are each worth 1 point unless otherwise indicated. Be clear and concise with any written answers. Graphs should be properly constructed (axis labels, units, titles, etc.)_*

__1.__ Paste in the output from `git log` performed at the end of the GitHub exercise.  Format this as a code block.

	bis180lstudent@bis180lstudent-VirtualBox:~/gh-usernames$ git log
	commit 23f3bb371edea149c3ccb409ccc2931bcb9da2e6
	Author: bis180lstudent <cjho@ucdavis.edu>
	Date:   Thu Apr 2 15:39:16 2015 -07
	
		Cjho3 changes
	
	commit 9088f60d278fc8d65a6c13a9e8117abd35bd37c2
	Merge: fa4557d a840556
	Author: jnmaloof <jnmaloof@ucdavis.edu>
	Date:   Thu Apr 2 15:20:29 2015 -0700
	
	    Merge pull request #3 from benroars/master
	    
	    added username
	
	commit a84055658a633157ec2bad99035fb0b68d45d1da
	Author: Ben Roa <benihanas1@gmail.com>
	Date:   Thu Apr 2 15:04:44 2015 -0700	
	    added username
	
	commit fa4557dcf2d515c0df93e676490621a2bd7d5175
	Author: Julin Maloof <jnmaloof@ucdavis.edu>
	:...skipping...
	commit 23f3bb371edea149c3ccb409ccc2931bcb9da2e6
	Author: bis180lstudent <cjho@ucdavis.edu>
	Date:   Thu Apr 2 15:39:16 2015 -0700
	
	    Cjho3 changes
	
	commit 9088f60d278fc8d65a6c13a9e8117abd35bd37c2
	Merge: fa4557d a840556
	Author: jnmaloof <jnmaloof@ucdavis.edu>
	Date:   Thu Apr 2 15:20:29 2015 -0700
	
	    Merge pull request #3 from benroars/master
	    
	    added username
	
	commit a84055658a633157ec2bad99035fb0b68d45d1da
	Author: Ben Roa <benihanas1@gmail.com>
	Date:   Thu Apr 2 15:04:44 2015 -0700
	
	    added username
	
	commit fa4557dcf2d515c0df93e676490621a2bd7d5175
	Author: Julin Maloof <jnmaloof@ucdavis.edu>
	Date:   Wed Apr 1 23:25:56 2015 -0700
	
	    added usernames file with info on Julin and Kristen
	
	commit 6f669219dafb3a316df9feda63c47cb38cfe1e88
	Author: jnmaloof <jnmaloof@ucdavis.edu>
	Date:   Wed Apr 1 22:58:56 2015 -0700
	
	    Initial commit
	~
	~
	~

__2.__ Paste in the output of `ls -lR Data` performed at the beginning of the Sequence_Alignment exercise.  Format this as a code block.

	drwxrwxr-x 4 bis180lstudent bis180lstudent 4.0K Apr  2 15:52 Sequences
	drwxrwxr-x 5 bis180lstudent bis180lstudent 4.0K Apr  3 14:01 Species
	bis180lstudent@bis180lstudent-VirtualBox:~/Data$ ls -lF
	total 8
	drwxrwxr-x 4 bis180lstudent bis180lstudent 4096 Apr  2 15:52 Sequences/
	drwxrwxr-x 5 bis180lstudent bis180lstudent 4096 Apr  3 14:01 Species/
	bis180lstudent@bis180lstudent-VirtualBox:~/Data$ ls -lR
	.:
	total 8
	drwxrwxr-x 4 bis180lstudent bis180lstudent 4096 Apr  2 15:52 Sequences
	drwxrwxr-x 5 bis180lstudent bis180lstudent 4096 Apr  3 14:01 Species
	
	./Sequences:
	total 8
	drwxrwxr-x 2 bis180lstudent bis180lstudent 4096 Apr  7 14:09 Genome
	drwxrwxr-x 2 bis180lstudent bis180lstudent 4096 Apr  7 02:38 Proteome
	
	./Sequences/Genome:
	total 0
	lrwxrwxrwx 1 bis180lstudent bis180lstudent 54 Apr  7 02:32 A.thaliana.fa -> /home/bis180lstudent/Data/Species/A.thaliana/genome.fa
	lrwxrwxrwx 1 bis180lstudent bis180lstudent 53 Apr  7 02:35 C.elegans.fa -> /home/bis180lstudent/Data/Species/C.elegans/genome.fa
	lrwxrwxrwx 1 bis180lstudent bis180lstudent 58 Apr  7 14:09 D.melanogaster.fa -> /home/bis180lstudent/Data/Species/D.melanogaster/genome.fa
	
	./Sequences/Proteome:
	total 0
	lrwxrwxrwx 1 bis180lstudent bis180lstudent 55 Apr  7 02:33 A.thaliana.fa -> /home/bis180lstudent/Data/Species/A.thaliana/protein.fa
	lrwxrwxrwx 1 bis180lstudent bis180lstudent 54 Apr  7 02:35 C.elegans.fa -> /home/bis180lstudent/Data/Species/C.elegans/protein.fa
	lrwxrwxrwx 1 bis180lstudent bis180lstudent 59 Apr  7 02:38 D.melanogaster.fa -> /home/bis180lstudent/Data/Species/D.melanogaster/protein.fa
	
	./Species:
	total 12
	drwxrwxr-x 2 bis180lstudent bis180lstudent 4096 Apr  3 14:03 A.thaliana
	drwxrwxr-x 2 bis180lstudent bis180lstudent 4096 Apr  3 13:48 C.elegans
	drwxrwxr-x 2 bis180lstudent bis180lstudent 4096 Apr  7 14:03 D.melanogaster
	
	./Species/A.thaliana:
	total 137888
	-rw-rw-r-- 1 bis180lstudent bis180lstudent 121183082 Apr  3 14:03 genome.fa
	-rw-rw-r-- 1 bis180lstudent bis180lstudent  20006289 Apr  3 13:47 protein.fa
	
	./Species/C.elegans:
	total 114484
	-rw-rw-r-- 1 bis180lstudent bis180lstudent 102292161 Apr  3 13:23 genome.fa
	-rw-rw-r-- 1 bis180lstudent bis180lstudent  14931762 Apr  3 13:48 protein.fa
	
	./Species/D.melanogaster:
	total 200188
	-rw-rw-r-- 1 bis180lstudent bis180lstudent 172113892 Apr  7 14:03 genome.fa
	-rw-rw-r-- 1 bis180lstudent bis180lstudent  32872415 Apr  7 14:03 protein.fa

__3.__ Fill in the following table.

|     Characteristic  |   A. thaliana    |   C. elegans   |   D. melanogaster
|:--------------------|:-----------------|:---------------|:-------------------
| File size           | 116 Mb|98 Mb | 165 Mb
| Chromosomes (#)     |        7    |     7           | 15
| Genome size (bp)    | 119,667,750|100,286,401| 168,736,537
| Protein-coding genes| 35,386 | 26,679 | 30,307
| Average protein (aa)|      415      |         455     | 673

__4.__ How do you know that when you use `shuffleseq` the sequences have the same exact composition?

We know this because shuffleseq doesn't add or remove any of the variables in the sequence, but instead changes the order or shuffles what is originally there. 

__5.__ Create a text based "histogram" as desribed in the lab manual that shows the distribution of scores when aligning 1000 shuffled C. elegans sequence "ce1" against the A. thaliana sequence "at1". Indicate with an arrow the score of the original, unshuffled alignment. Why is the shape of the curve not quite normal?  Format this as a code block.

  	    1 24.0
  	    1 27.0
  	    3 29.0
  	    2 31.0<--
  	    1 32.0
  	    1 33.0
  	    2 34.0
  	    1 35.0
  	    1 36.0
  	    1 38.0
  	    1 39.0



The curve is not quite normal because there is a slight skew to one of the ends, where there is a higher frequency of repeated score values.

__6.__ Perform the experiment 3 more times with a different 1000 shuffled sequences. Create a table using markdown with the mean, mode and median for each run (include your first run for a total of 4 runs).

|                       | Run 1 | Run 2 | Run 3| Run 4
|:--------------------|:-----------------|:---------------|:-------------------|:-------------------
|Mean|32.0667 |31.836 |31.8229 |  31.8981
|Mode| 29.0 |30.0 |31.0|31.0
|Median| 38.5| 24.0|24.0|24.0

__7.__ What would be the effect of doing more than 1000 shuffled sequences?

The likely effect of doing more than 1000 shuffled sequence would be that there would be very similar values to that of which was observed from the 1000 shuffled sequences.

__8.__ Briefly discuss the relationship of sequence length and score.

The relationship between sequence length and score are directly associated to the gap value parameters that are chosen in each test. This is because the length of a sequence can vary based on where gaps are and this will in turn change the alignment score.

__9.__ Search the ce1 sequence against a shuffled version of the same sequence and report the average score.

33.4667

__10.__ Create a fake protein sequence containing 50% Q but the rest of the letters are typical of real proteins (add a bunch of Qs to the end of a real sequence). Now make a shuffled version of this to distribute the Qs around. Search this against the ce1 and at1 sequences and report the alignment score.

	22.0
	27.0
	29.0
	31.0
	31.0
	32.0
	32.0
	33.0
	34.0
	34.0
	35.0
	35.0
	36.0
	38.0
	51.0
average score of 33.33 with ce1 

	22.0
	25.0
	26.0
	27.0
	28.0
	28.0
	29.0
	30.0
	30.0
	31.0
	32.0
	33.0
	36.0
	39.0
	46.0
average score of 30.8 with at1

__11.__ Create 1000 shuffles of the Q-enriched sequence above and report the average score.

31.405 with at1 and 33.7196 with ce1

__12.__ Briefly discuss parts 9-11 with respect to how sequence composition affects score. (*2pts*)

Sequence composition affected the score because when shuffled, the 50% composition of Q didn't really change the average alignment score. This means that because there were so many Q added, that it allowed for many different alignment sequences, and probably conserves the score to some degree.

__13.__ Perform random alignments (as in question 4 above) with the following different alignment scoring schemes:

|     Matrix    |   Gap Open    | Gap Extend |   Mean  | Mode    | Median
|:--------------|:--------------|:-----------|:--------|:--------|:--------
| EBLOSUM80     |       9       |     3      | 57.2667 |  59.0  |73.5
| EBLOSUM80     |       9       |     9      |     49.8 |     54.0    |62.5
| EBLOSUM40     |       9       |     3      |    128.8     |    all in equal proportion     |    181.0
| EBLOSUM40     |       9       |     9      |   96.8      |    89.0     | 129.5
| EBLOSUM62     |       9       |     3      |     32.1333    |      36.0   |    37.5         
| EBLOSUM62     |       9       |     9      |      31.8667   |     33.0    |      37.5

_Hint:_ You can use the spreadsheet application "gnumeric" (relevant functions are average(), mode(), and median()).  Or you can use R.

__14.__ Inspect the scoring matrices in `/usr/share/EMBOSS/data`. Briefly discuss the table above with
respect to the scoring parameters. (*2pts*)

The highest alignment score values were from the EBLOSUM40 runs. This is to be expected since this parameter constricts the test for the percent identity match to be below 40%. This therefore allows the test to have many more gaps, and muc longer sequence lengths than those of the EBLOSUM80 and 62.

__15.__ Starting with the C. elegans B0213.10 protein, find the best match in the A. thaliana and D.melanogaster proteomes with `water`. Record their alignment scores and protein names here.

A.thaliana: AT5G06905.1, score: 17.0

D.melanogaster: FBpp0289274, score: 13.0

__16.__ What is the expected score of each protein at random? (Perform some shuffled alignments
to get an idea of what the random expectation is).

The expected score for AT5G06905.1: 26.0
					FBpp0289274: 24.0

__17.__ Briefly discuss the statistical and biological significance of your results. (*2pts*)

Biologically this is significant because this could show preference for this protein throughout  evolutionary history. Statistically, this is signifanct because this shows that this isn't completely due to random chance.
