<H3>Metagol NT</h3>
<br>
MetagolNT is a nois telorant version of Metagol. This version is implemented based on the paper 
   <a href="https://link.springer.com/article/10.1007/s10994-018-5710-8">Meta-Interpretive Learning from noisy images</a>.
   <br>
A normal version of metagol is developed by <b>Andrew Cropper</b> and available from the [GitHub](https://github.com/metagol/metagol). All sample code and settings can be found from former link.

#### Using Metagol NT
MetagolNT is written in Prolog and runs with SWI-Prolog.<br>
Copy the <b>metagolNT.pl</b> file into your project's folder.<br>
Include metagolNT to your project: 

```prolog
:- use_module('metagolNT').
```
#### Learn from examples
##### learnNT(POS,NEG,NoisLevel,Iteration,Verbos)
The predicate learn requires 5 arguments including positive examples, negative example, nois telorance, number of iterations and verbos:
``` Prolog
learnNT(Pos,Neg,33,10,true).
```

The following code demonstrates learning from a few simple background knowledge and examples:
``` Prolog
:- use_module(metagolNT).

body_pred(add/2).

metarule([P,Q],[P,A,B],[[Q,A,B]]).

add(1,2).
add(2,4).
add(3,6).
add(4,8).

:-
        %------example,example,nois ------%
        Pos = [mul(1,2),mul(3,6),mul(4,7)],
        Neg = [mul(1,1),mul(3,3),mul(4,4)],
        learnNT(Pos,Neg,33,10,true).
```
#### Bug Reports and Feature Requests
Please submit all bug reports and feature requests as issues on this GitHub repository or by contacting [Daniel Cyrus](mailto:d.cyrus@surrey.ac.uk?subject=[GitHub]MetagolNT_bug).
