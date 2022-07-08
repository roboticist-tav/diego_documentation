# Ranking (setter)



## set_ranking
Sets the ranking calculation to use when analysing results of polls and statistics for decisions.
#### set_ranking(*rank_type*)
| ```rank_type``` | Description |
|:--:|--|
| ```std_comp``` | Uses *standard competition ranking*, also known as "1224" ranking. |
| ```mod_comp``` | Uses *modified competition ranking*, also known as "1334" ranking. |
| ```dense``` | Uses *dense ranking*, also known as "1223" ranking. |
| ```ordinal``` | Uses *ordinal ranking*, also known as "1234" ranking. |
| ```fract``` | Uses *fractional ranking*, also known as "1 2.5 2.5 4" ranking. |
^See^ ^https://en.wikipedia.org/wiki/Ranking^ ^for^ ^more^ ^information.^
#### set_ranking(*rank_type*)_to(*moniker1*, *n...*)