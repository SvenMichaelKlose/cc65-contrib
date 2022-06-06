Randfade V1.0 30.11.2006 compiled with ccs65 v11.0
--------------------------------------------------

This is a small demo of how to fade out a textscreen by 
setting chars at random positions, so that the former contents 
of the screen will be overwritten more and more. 

Algorithm:

On a 40x25 display there are at first m=1000 positions, where a
char could be placed to overwrite a character.
After that, only m=999 positions are left to be overwritten.
The next char can be placed only on one of these 999 position, 
because we don't want to place a char two times at the same x/y coord.
After 1000 steps, the screen is filled completely. 

Steps:

1) Set up a table t with m entries from 0 to m-1
2) Generate a random number x between 0 and m-1 
3) Overwrite the char at the screen position t[x]
4) Update the table t[y!=x]->t[x] 
	(Choose y to be not equal to x, for example: y=m-1)
5) Decrease m
6) goto 2)
