# Sittinun_work
 2020 / 09 / 23 
 This mini self-project applied Natural language processing to do cleansing data in reasearch titles by tokenization.
 
 required 
 ------------
 1. pyspark
 2. findspark
 3. pythainlp 2.2.2 --> engine 'Multi-cut'
 4. nltk 2.5
 5. pandas
 
 Problem
 ------------
 We want to count a number of research titles about 'dust' meaning dust poluution, but we face double counting problem from other words simultaneously such as industry. 
 
 Case studies
 ------------
 English case: Instead we detect word 'dust' meaning dust pollutions, but we get word 'industry',because dust is a component of word 'in-dust-ry'.
 Thai case   : Quite similar to above case Instead of word 'เดิน'(walk meaning in Thai), we get word 'ดิน'(soil meaning in Thai).
 
 Question 
 ------------
 How can we scan title with keyword 'dust', then we get title relating to 'dust' meaning dust pollutions not industry.         
 
 Solution
 ------------
 One of my solutions is using words tokenization with those strings so as to get back a of words representing the titles.  
 
 Concept
 -------------
 I import 2 modules, nltk and pythainlp, in order to tokenize titles. Because nltk could only tokenize english language, so we had to design process separating english
 titles from thai titles. Now we've already known the titles tokenized by nltk give a length of list which involve approximately more than 10.We label titles that have length over 10 as 'Eng' ;otherwise, we feed them to next process. The rest of titles haven't label yet, we asume those are thai titles, then we used
 pythainlp to tokenize them and label as 'TH'. Finally, we concat them together turning to single table and upload to main database.  

Output
-------------
Column of word tokenization after research titles. We scan keyword this column instead of research titles.

Weakness point
--------------
It depend on engine that we use lead to some error.       
 
 
 
 
 
 
 
 
