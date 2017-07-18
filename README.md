\d = digit
\. = match a dot ('.') since dot ('.') is wildcard in regex, have to escape it
[] = match specific characters by putting them inside square brackets. 
[^abc] = ^ = dont match these characters. For EG [^abc] would ignore all abc s in string (only means this in context of being inside [])
- = can be used in [ ] to match characters rangers [a-z]. Can use w/ whatever [^b-d]
\w = equivalent of "all standard characters" [A-Za-z0-9_]

Repition
\d\d\d = match 3 digits
aaa = match 3 'a'
{ } = how many characters to match
a{3} = match 3 'a'

Some regex engines allow a{1, 3} which matches 'a' no more than 3 and no less than 1

Other examples
[wxy]{5} = five characters, each of which can be a w, x, or y
.{2,6} = between two and six of any character

* = to infinity and beyond. represents 0 or more of the character it follows. Its called Kleene Star for some reason.
+ = 1 or more of the character that it follows. Kleene Plus. 

examples
\d* = get any number is digits (including none). 
\d+ = get any number is digits, and insures there is at least 1 digit
a+  = one or more a 
[abc]+ = one or more of any a, b, or c character
.* = zero or more of any character

? = optional stuff. matchs either zero or one of the characters or group

example
ab?c will match either "abc" or "ac" because the b is optional

\s = match whitespace. (takes into account new line / tab / space)

^ $ = describe the start and end of a line 

example
^success = only match Sentances starting with 'success'
t$ = would match the 't' in 'eat'


( ) = use to match groups
https://regexone.com/lesson/capturing_groups?

( ()) = can match groups in groups 
https://regexone.com/lesson/nested_groups?

| = or. like (cats|dogs)

\D = non-digit char
\S = non-whitespace char
\W = non-alphanumeric char (eg punctuation)

\b = matches the boundary between a word and a non-word character
Its most useful in capturing entire words (for example by using the pattern \w+\b).





