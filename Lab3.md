Lab#3 - CSCI 3155

Mark Ariniello, Ahmed Alshakh

###problem 2 

### C

In evaluating e1 ----> e1' we are always going to be evaluating e1 first and then e2, which makes these judgements deterministic. In addition whenever we have e2 -----> e2' there is no e1 because it has already been evaluated to v1.

###problem 3

In e1 + e2, e1 has precedence due to:

e1 -----> e1

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

e1bope2 ----->e1'bope2

where e1 is evaluated to e1' in order to change the order you should swicth which equation you evaluate first
so before you do e1, do e2.

e2 -----> e2

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

e1bope2 -------> e1bope2'

since this has e2 evaluated to e2' before e1 is evaluated.

###problem 4 

### A

Short circuiting is important in the logical operations && and ||, in the first one you can speed up a program significantly by exiting out if the first condition is false, 

EX: if (a&&b) do {stuff}; if a = false, then we don't care about b because the expression will return false anyways.
this is similar to the 0*a = 0 question, since anything times 0 = 0 and would save time on the calculation.

EX: if (a||b) do {stuff}; if a = true in this case, there is no need to see if b is true since we already know that 
we should do stuff. Again short circuting is extremly important if figuring out weather or not b is true would tak a long amount of time.

EX: if ((3-a > 0) && (15*25^b/64 + c%n)) {stuff} in this case a is a much simpler program to run than b, so in order to save on time, if a is false we can skip b, because && allows us to short circuit if it was :
if ((3-a > 0) & (15*25^b/64 + c%n)) {stuff} and a > 3 then we would still have to execute all of the code to the right of the & even though we knew that the conditional was false.

### B

The small step schmantics for e1 && e2 do short circut becasue 

false = toBoolean(v1)

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

v1 && e2 ------> v1

Which causes the false value to be used for the conidtional (e1 && e2) where as if it didn't short circuit it would evaluate e2 ---> v2 and see if v1 & v2 was true.




