<H3>Metagol NT</h3>
<br>
MetagolNT is a nois telorant version of Metagol. This version is implemented based on the paper 
   <a href="https://link.springer.com/article/10.1007/s10994-018-5710-8">Meta-Interpretive Learning from noisy images</a>.
   <br>
A normal version of metagol is developed by <b>Andrew Cropper</b> and available from the [GitHub](https://github.com/metagol/metagol). All sample code and settings can be found from former link.
<br><br>
<b>Using MetagolNT</b><br>
MetagolNT is written in Prolog and runs with SWI-Prolog.<br>
Copy the metagolNT.pl file in your project's folder.<br>
Include metagolNT to your project: 
inline code- `:- use_module(metagolNT).`
Learn from examples.
block code-
``` Prolog
learnNT(Pos,Neg,33,10,true).
```
