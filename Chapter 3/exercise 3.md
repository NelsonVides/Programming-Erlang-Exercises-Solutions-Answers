```erlang

77> H1 = {house, "3 Maple St"}.  
{house,"3 Maple St"}

78> H2 = {house, "5 Maple St"}.
{house,"5 Maple St"}

79> H3 = {house, "7 Maple St"}.
{house,"7 Maple St"}

80> Street = [H1, H2, H3].
[{house,"3 Maple St"},
 {house,"5 Maple St"},
 {house,"7 Maple St"}]
 
81> [{house, Addr} | Tail] = Street.
[{house,"3 Maple St"},
 {house,"5 Maple St"},
 {house,"7 Maple St"}]
 
82> Addr.
"3 Maple St"

83> Tail.
[{house,"5 Maple St"},{house,"7 Maple St"}]

84> f(Addr).    %"forget" (or unbind) the Addr variable. Or use a different variable name in the expressions below.             
ok

85> [_, _, {house, Addr} | [] ] = Street.   %This syntax is described on the bottom of p. 38. See below for alternative syntax.
[{house,"3 Maple St"},
 {house,"5 Maple St"},
 {house,"7 Maple St"}]
 
86> Addr.
"7 Maple St"

%This syntax also seems to work:

87> f(Addr).                             
ok

88> [_, _, {house, Addr}] = Street.      
[{house,"3 Maple St"},
 {house,"5 Maple St"},
 {house,"7 Maple St"}]
 
89> Addr.
"7 Maple St"
```
