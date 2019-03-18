# Cryptography-Term-Project
Coded toy version of RSA algorithm

Project 1.

Your task is to write a program (Java or C++) that decrypts a ciphertext encrypted with a toy version of RSA that uses a small value for n. Your program should work with any n <= 100000. The input of your program consists of the public key (n, e) and the ciphertext given as a sequence of numbers.

Below is one RSA ciphertext which you will use to test your program. The public key used for the encryption (but your program should handle any parameters having the above order of magnitude) is, in this example, n = 18923 and e = 1261. Decryption will be done as follows. First factor n (which can be done  because n  is <= 100000), then compute the exponent d as the inverse of
e mod (p-1)(q-1) using the extended Euclidean algorithm, and finally, decrypt the ciphertext..  Don’t take any function from a crypto library.  In particular, write your own version of the extended Euclidean algorithm and your own version of modular exponentiation using the repeated squaring method.  (Note: there will be penalties in the grade if you implement simpler algorithms than these two).

In order to translate into English text you need to know how text is converted into numbers (at encryption time). The text is broken into blocks of three letters and then each block is converted into a number as you can see in the examples below:

dog  3 * 262 + 14 * 26 + 6 = 2398
cat  2 * 262 + 0 * 26 + 19 = 1371
zzz -> 25 * 262 + 25 * 26 + 25 = 17575

You will have to invert this process as the final step of the decryption.

The program has to be written entirely by you (you are not allowed to use any software other than the Java or the C++ compiler with the standard libraries; in particular, you are not allowed to use the Crypto or the BigInteger libraries). Your program must contain functions for
Factoring 
Computing the multiplicative inverse in modular arithmetic using the extended Euclidean algorithm
Modular exponentiation using the repeated squaring method
Converting from numbers back to text (Note: You need to invert the above procedure which converts from text to numbers).

You will turn a report containing:  (a) a brief description of your program, (b) the source code in Java or C++, (c) the plaintext.  Make your program modular, including the functions listed above, and try to make it as general as possible   In the description (a) include the list of functions with their parameters. Comment your program appropriately. You should be prepared to do a demo of your program. The grade will depend on all three elements: (a), (b), and (c), so give attention to all of them.


Ciphertext encrypted using RSA (Each number in the ciphertext represents three alphabetic characters as explained above):



12423	11524	7243	7459	14303	6127	10964	16399
9792	13629	14407	18817	18830	13556	3159	16647
5300	13951	81	8986	8007	13167	10022	17213
2264	961	17459	4101	2999	14569	17183	15827
12693	9553	18194	3830	2664	13998	12501	18873
12161	13071	16900	7233	8270	17086	9792	14266
13236	5300	13951	8850	12129	6091	18110	3332
15061	12347	7817	7946	11675	13924	13892	18031
2620	6276	8500	201	8850	11178	16477	10161
3533	13842	7537	12259	18110	44	2364	15570
3460	9886	8687	4481	11231	7547	11383	17910
12867	13203	5102	4742	5053	15407	2976	9330
12192	56	2471	15334	841	13995	17592	13297
2430	9741	11675	424	6686	738	13874	8168
7913	6246	14301	1144	9056	15967	7328	13203
796	195	9872	16979	15404	14130	9105	2001
9792	14251	1498	11296	1105	4502	16979	1105
56	4118	11302	5988	3363	15827	6928	4191
4277	10617	874	13211	11821	3090	18110	44
2364	15570	3460	9886	9988	3798	1158	9872
16979	15404	6127	9872	3652	14838	7437	2540
1367	2512	14407	5053	1521	297	10935	17137
2186	9433	13293	7555	13618	13000	6490	5310
18676	4782	11374	446	4165	11634	3846	14611
2364	6789	11634	4493	4063	4576	17955	7965
11748	14616	11453	17666	925	56	4118	18031
9522	14838	7437	3880	11476	8305	5102	2999
18628	14326	9175	9061	650	18110	8720	15404
2951	722	15334	841	15610	2443	11056	2186

