# Grammar
program ::=
{definition}O
definition ::=
name {[ {constant}& ]}~ {ival {t ival}o]$ ;
name ( {name {9 name}O}~ ) statement
ival ::=
constant
name
statement ::=
auto name {constant}: {, name {constant}~}O ; statement
-—
extrn name {, name}. ; statement
-—
name : statement
case constant : statement
-—
{ {statement}. ]
if ( rvalue ) statement {else statement}~
—-
while ( rvalue ) statement
-— .
—.\
switch rvalue statement
. ●
-3-
goto-rvalue ;
-—-
return {( rvalue )}: ;
—- --
{rvalue}~ ;
rvalue ::=
( rvalue )
lvalue
constant
lvalue assign rvalue
inc-dec lvalue
.
lvalue inc-dec
unary rvalue
& lvalue
rvalue binary rvalue
rvalue ? rvalue : rvalue
rvalue ( {rvalue {, rvalue}O }: )
assign ::=
= {binary}:
inc-dec ::=
++
--
--
.-
unary ::=
!
binary ::=
I
I
&
==
—-
,
. ,
-4-
!=
<
<=
>
>
=
<<
—
>>
—
+
‘%
*
lvalue ::=
name
* rvalue
rvalue [ rvalue ]
constant ::=
{digit},
* {char}f’ ‘
“ {char}O “
name ::=
alpha {alpha-digit}:
alpha-digit ::=
alpha
digit