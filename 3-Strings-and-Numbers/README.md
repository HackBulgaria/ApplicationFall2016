# Strings and Numbers

You are given a string `s` that consists of characters, that encode digits & characters that encode nothing. Your goal is to return the sum of all numbers in that string.

## Number encoding

In our string `s`, the digits from `0` to `9` are encoded as follows:

* `9` is encoded with the most repeated character in `s`.
* `8` is encoded with the most repeated character in `s`, that comes after the one that encodes `9`.
* `...`
* `0` is encoded with the most repeated character in `s`, that comes after the one that encodes `1`.

For example, if `9` is encoded with `a`, which is repeated `16` times in `s`, `8` can be encoded with `x`, which is repeated `15` times in `s`.

## Input details

* You read one line from the standard input - the encoded string.
* You are guaranteed that there won't be two digits encoded with the same number of repeating characters.
* There will always be encoding for all digits between `0` and `9`.
* Not all digits from `0` to `9` can be encoded. We can have shorter strings that encode small number of digits.
* There will always be enough characters to encode digits from `0` to `9`.
* Input set is `"abcdefghijklmnopqrstuvwxyz!"#$%&\'()*+,-./:;<=>?@[\\]^_{|}~"`
* If after decoding there are numbers with leading zeroes, ignore them.
* Results can get very large. Tackle it with big integers.

Output should be the sum of all numbers in the string.

## Examples

Let `s = "bbcccddddeeeeeffffffggggggghhhhhhhhiiiiiiiiijjjjjjjjjja"`

We have the following encoding:

* `j` is repeated `10` times so `j = 9`
* `i` is repeated `9` times so `i = 8`
* `h` is repeated `8` times so `h = 7` 
* `g` is repeated `7` times so `g = 6` 
* `f` is repeated `6` times so `f = 5`
* `e` is repeated `5` times so `e = 4`
* `d` is repeated `4` times so `d = 3`
* `c` is repeated `3` times so `c = 2`
* `b` is repeated `2` times so `b = 1`
* `a` is repeated only once so `a = 0`

Now, if we decode our string, we get: `s = "1122233334444455555566666667777777788888888899999999990"`

Since there are no other characters, the sum of that all numbers in the string is `1122233334444455555566666667777777788888888899999999990`.

----

Lets take a look at another example:

Let `s = "}w#\a:\?uxv?xvxx@axx?\u\^:a~wx?x-:u\v\a:???^xv?x??cwwx_?uhvc:w<v,:ucwzuaw::uaucwaa^ra:;?:\?xbw[^^:w::ca\wcvl\:%"`

After decoding, our string will look like this: `"}6#4594837287277@5778434095~6787-934245988807287881667_83h2196<2,9316z3569935316550r59;89487b6[009699154612l49%"`

This yields the following result: `6 + 4594837287277 + 5778434095 + 6787 + 934245988807287881667 + 83 + 2196 + 2 + 9316 + 3569935316550 + 59 + 89487 + 6 + 9699154612 + 49 = 934245996987538182192` 

----

Another example:

* `s = "pr$pprtppp{%r%%#(;%rn$;~*s%r%r%;(#(x$p([~(~(r}%=([$[#[~[;~+rr~[r#(n([r%(n%b~;p#rp($;$[,l?(n~p#%$prn~%$r#(~$"`
* `decoded = "694669t666{7977281790415*s797971828x468358589}7=8343235315+995392808397807b51629684143,l?805627469057492854"`
* `result = 694669 + 666 + 7977281790415 + 797971828 + 468358589 + 7 + 8343235315 + 995392808397807 + 51629684143 + 805627469057492854 = 806630900387626293`

----

Another example:

* `s = "|?=xi^.k%x||^cs^s^=||x=x|.&=..|=x=|&kv^^jkt&jzx.xx=|&&!jkjs&kj|x>j.!..^&k..&k||o&s|s=j.xx!x)j=!&s&]n|^j.!jx"`
* `decode = "9?48i372%8993c13134998489764779484962v3352t65z878849660525162598>57077362776299o61914578808)540616]n9357058"`
* `result = 9 + 48 + 372 + 8993 + 13134998489764779484962 + 3352 + 65 + 878849660525162598 + 57077362776299 + 61914578808 + 540616 + 9357058 = 13135877396564591913180`
