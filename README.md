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
 How can we classify dust out of industry or ดิน out of เดิน?  
 
 Solution
 ------------
 One of my solutions is Using words tokenization with those strings so as to get back a lists of words representing the titles.     
 
 
 
 
 
 
 
