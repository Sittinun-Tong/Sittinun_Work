# Sittinun_work
2020 / 09 / 23 
 This self-project applied Natural language processing to do cleansing data in reasearch titles by tokenization.
 
 required 
 1. pyspark
 2. findspark
 3. pythainlp 2.2.2 --> engine 'Multi-cut'
 4. nltk 2.5
 5. pandas
 
 Problem is how can we know keywords that we want to detect is correct 
 
 English case: Instead we detect word 'dust' meaning dust pollutions, but we get word 'industry',because dust is a component of word 'in-dust-ry'.
 Thai case: Quite similar to above case Instead of word 'เดิน'(walk meaning in Thai), we get word 'ดิน'(soil meaning in Thai).
 
 solution is   
 
 
 
 
 
 
