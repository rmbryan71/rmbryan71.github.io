# Counting DNA Nucleotides
[This](https://rosalind.info/problems/dna/) problem asks:

**Given**: A DNA string _s_ of length at most 1000 nt.

**Return**: Four integers (separated by spaces) counting the respective number of times that the symbols 'A', 'C', 'G', and 'T' occur in _s_.

## First impression
They're going to send me a string of text no longer than 1000 characters.

They want me to count the A's, C's, G's and T's, then return those results.

This is so easy, I would call it "[trivial](https://science.awjunaid.com/math/difference-between-trivial-vs-non-trivial-problem/)", except it does involve some file handling. 

## Solution Steps
The way [Project Rosalind](https://rosalind.info/about/) works is that you click a big "Download Dataset" button and the website deposits a file in your downloads folder.
This problem's abbreviation is "dna", so the download file will be called "rosalind_dna.txt"

Then you have 5 minutes to upload your answer. 

Since time is limited and we don't want to waste time looking for files or moving them around, we'll start our program by opening the specific file in the downloads folder.

Then we just count.

Python includes a [list count method](https://www.w3schools.com/python/ref_list_count.asp) that solves this problem for us.

To be fancy, I'm using a little helper program (package) called pyperclip to drop the answer onto my clipboard so all I have to do is paste it in the answer box.

## Conclusion
This is the easiest problem in the set, by far.

Things will get more interesting as we go along.



