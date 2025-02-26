java c
CS-265/CSC325 Artiﬁcial   Intelligence – Coursework   1   [15 marks] 
Deadline:   6   March   2025,   11am   GMT 
Task   Description Consider   the   following   situation:    Assume   you    have   a   database   of   articles,   together   with   their   length   in   words   and   the   topics   covered.      Using   graph   search   you   want   to   create   an   information   brochure   that   is   as   concise   as   possible,   i.e.,   as   short   as   possible   while   covering   all of the required topics.    The   article database contains   the   ﬁve   articles   in   the   table   below.
Table   1:   Database   of articles,   their   length   and   topics   covered.
Article 
Length in words 
Topics Covered 
art0 
200 
[introduction] 
art1 
600 
[industry 5.0, challenges] 
art2 
1000 
[introduction, human-centric design, cobots] 
art3 
800 
[infographic, skills] 
art4 
1000 
[industry 5.0, cobots] In   the   search   graph,   a   node   is   a   pair   (To Cover,   Articles〉where   Articles   is   a   list   of   articles   that      must   be      in   the   brochure,      and   To Cover is      a      list   of   topics   that      have   to   be   covered.
•   The   neighbours   of a   node   are   obtained   by   ﬁrst   selecting   a   topic   from   To Cover.
•   There   is   a   neighbour   for   each   article   that   covers   the   selected   topic.
•   The   remaining   topics   are   the   topics   not   covered   by   the   articles   added   so   far.Assume that the leftmost   topic   is   selected   at   each   step.    For instance,   given the   database      shown in Table   1, the neighbours of   the node   ([introduction,   cobots], []〉, when ‘introduction’   is   selected,   are   ([], [art2]〉and   ([cobots], [art0]〉.   Thus,   each   arc   adds   exactly   one   article   but    can   cover   (a代 写CS-265/CSC325 Artificial Intelligence – Coursework 1Matlab
代做程序编程语言nd   so   remove)   one   or   more   topics.      Suppose   that   the   cost   of the   arc   is   equal   to      the   word   count   of the   article   added.
The   goal   is to   design   a   brochure that   covers   all   of the topics   in the   list   Must Cover.    The   starting   node   is   (Must Cover, []〉.    The   goal   nodes   are   of   the   form   ([],   Brochure〉.    The   cost   of the path from a start node to a goal node is the length of   the articles used.    Thus, an optimal   brochure   is   a   shortest   collection   of articles   that   covers   all   of the   topics   in   Must Cover.
(a)    Suppose   that   the   goal   is   to   cover   the   topics   [introduction,   industry 5.0,   cobots]   and   the   algorithm   always   selects   the   leftmost   topic   to   ﬁnd   the   neighbours   for   each   node.   Draw the search space expanded   for   a   Greedy   search.    Number the nodes   in   the   order   of expansion until a solution is found.    Nodes that are not considered   should   not   carry   a   number.   Your   search   tree   should   include   all   nodes   expanded,   highlight   which   node   is   a   goal   node,   and   show   the   frontier   when   the   goal   was   found.                                                 [9   marks]
(b)    Give a non-trivial admissible heuristic   function   h.    [Note   that   h(n)   =   0   for   all   nodes   n   is the trivial   heuristic   function.]    Does your   heuristic   satisfy the   monotone   restriction   for   a   heuristic   function?                                                                           [3   marks]
(c)    Does   the   order   of   topics   selected   in   the   expansion   of   the   search   space   inﬂuence   the   result   found?      Justify   your   answer.                                       [3   marks]



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
