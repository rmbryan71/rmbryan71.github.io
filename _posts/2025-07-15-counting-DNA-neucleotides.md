---
layout: post
title:  "Counting DNA Nucleotides"
date:   2025-07-15
---

[This](https://rosalind.info/problems/dna/) problem asks:

> **Given**: A DNA string _s_ of length at most 1000 nt.

> **Return**: Four integers (separated by spaces) counting the respective number of times that the symbols 'A', 'C', 'G', and 'T' occur in _s_.

## First impression
They're going to send me a string of text no longer than 1000 characters.

They want me to count the A's, C's, G's, and T's, then return those results.

This is so easy, I would call it "[trivial](https://science.awjunaid.com/math/difference-between-trivial-vs-non-trivial-problem/)", except it does involve some file handling.
## Mechanisms
The way [Project Rosalind](https://rosalind.info/about/) works is that you click a big "Download Dataset" button and the website deposits a file in your downloads folder.
This problem's abbreviation is "dna", so the download file will be called "rosalind_dna.txt"

Then you have 5 minutes to upload your answer. 

Since time is limited and we don't want to waste time looking for files or moving them around, we'll start our program by opening the specific file in the downloads folder.
For me, that's '''file_path = "/Users/robertbryan/Downloads/rosalind_dna.txt"'''

## Solution steps
Python includes a [list count method](https://www.w3schools.com/python/ref_list_count.asp) that solves this problem for us.

Then we just count all the A's, C's, G's, and T's.

```aiignore
    return (
        sequence.count("A"),
        sequence.count("C"),
        sequence.count("G"),
        sequence.count("T")
    )
```

I write my results to a text file so that I can upload them easily.
## Inefficient solution
My solution ran on the test set in less than a second, but it's not the fastest solution because it has to go all the way through the test set four times.
Once to count the A's, once to count the C's, etc...

Since the problem tells us the maximum number of letters in the test set is 1000, and we have 5 minutes to solve the problem, my inefficient solution that takes less than a second is fine.

If I wanted to make my solution faster over much larger datasets, I would set up four counters: A, C, G, and T. Then I would run through the list one time and increment the counter that matches the letter in the test set, but I don't care about the extra time, so my simple solution is fine for this purpose.

## Conclusion
This is one of the easiest problems in the set.

Things will get more interesting as we go along.



