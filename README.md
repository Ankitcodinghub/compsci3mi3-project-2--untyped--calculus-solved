# compsci3mi3-project-2--untyped--calculus-solved
**TO GET THIS SOLUTION VISIT:** [COMPSCI3MI3 Project 2 –Untyped λ-Calculus Solved](https://www.ankitcodinghub.com/product/compsci3mi3-project-2-untyped-%ce%bb-calculus-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;92583&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COMPSCI3MI3 Project 2 –Untyped λ-Calculus Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="section">
<div class="layoutArea">
<div class="column"></div>
</div>
</div>
<div class="layoutArea">
<div class="column">
Part 1: Implementing Untyped λ-Calculus

<ol>
<li>Term Definitions
The grammar of the untyped λ-Calculus is given below.

⟨t⟩ ::= ⟨Var⟩

| λ⟨Var⟩.⟨t⟩ | ⟨t⟩⟨t⟩

⟨Var⟩ ::= A | B | C | D | E | F | G | H | I | J | K | M | N | O | P | Q | R | S | U | V | W | X | Y | Z

Unlike our terms of UAE, in λ-Calculus, we need to be able to handle something close to the idea of algebraic variables. So, we will add the following restriction. In our Haskell implementation, what we mean by “variable” is one element from a set of labels. This set contains every letter of the standard English alphabet. You are allowed to skip a few of these if you are using them in your term data type.

Implement this grammar as a recursive datatype in Haskell. Both data types will need to derive Eq, and it would be convenient for them to also derive Show.
</li>
<li>Free Variables

Implement a function which takes in a term as defined above, and returns a list containing the free</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
variables in that

FV(x) = FV(λx.t1) = FV(t1t2) =

This will require

</div>
<div class="column">
term. The rules for finding these are as follows:

{x} FV(t1)\{x}

FV (t1) ∪ FV (t2)

use of Haskell lists. You may find some of the functions in Data.List useful:

</div>
</div>
<div class="layoutArea">
<div class="column">
• union

• \\

• nub (as a last resort!)

For more information, check the documentation at https://hoogle.haskell.org/

<ol start="3">
<li>&nbsp;Relabelling

In order to implement our rules of substitution, we will need a way to relabel terms. In general, terms that differ only in the names of bound variables are interchangeable in all contexts. Write a function in Haskell which, given a term, the name of a variable to replace, and the name of a variable to replace it with, replaces each occurrence of the first variable with the second.

You may assume all occurrences of the variable we are replacing are bound. You may also assume that, if a subexpression contains a lambda abstraction over the same variable name, that we are replacing that variable name too.
</li>
<li>Substitution

The rules of substitution are given as follows:</li>
</ol>
</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Write a function in Haskell named sub which performs substitution over the terms defined in question 1. This function should accept as arguments:

• The term the substitution is being performed on • The variable label being substituted out.

• The term that is being substituted in.

Your function should also implement the meta-rule implicit in the above substitution rules, that if the abstracted variable is in the set of free variables of the term being substituted in, it must be relabelled with a label that does not conflict with any of the other labels. The function you wrote in the previous part should help with that.

The function should output the term produced as a result of the substitution operation.

<ol start="5">
<li>&nbsp;Normal Forms

Write a Haskell function, isNF which accepts as an argument a term of our calculus, and outputs a Boolean value (that is, a Haskell Bool, not a Church Boolean). This function must determine whether or not a term is in normal form, according to the call by value evaluation strategy.</li>
<li>&nbsp;Small Step Operational Semantics

Consider the operational semantics of the call by value evaluation strategy of λ-Calculus.

Using these operational semantics, write a function, ssos. This function will take a term as input, and will output the result of a single step of our call by value evaluation strategy.
</li>
<li>&nbsp;Full Evaluation Write a function, eval, which, when applied to a term, fully evaluates it.
Part 2: Implementing Some Functions

When you have completed this section, submit the code as ULC2.hs to the Avenue dropbox.
</li>
</ol>
8. Boolean Functions

</div>
</div>
<div class="layoutArea">
<div class="column">
Page 2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
<ol>
<li>(a)&nbsp; Logical Not

Write a Haskell function which uses your newly developed λ-Calculus to implement a logical not operation over Church Booleans. This function should take a term of our calculus, and return a term of our calculus. You are not allowed to use pattern matching for this question!</li>
<li>(b Logical And

Repeat the above for a logical and operator. This function should take two terms of our calculus, and return a third.</li>
<li>(c)&nbsp; Logical Or

Repeat the above for a logical or operator. This function should take two terms of our calculus, and return a third.</li>
</ol>
9. Numeric Functions

<ol>
<li>(a)&nbsp; &nbsp;Numeric Sum

Write a Haskell function which uses your newly developed λ-Calculus to implement addition over church numerals. This function should take two terms of our calculus and return a third. You are not allowed to use pattern matching for this question, you have to do it exclusively in λ-Calculus!</li>
<li>(b)&nbsp; Numeric Times

Repeat the above for a numeric multiplication operator. This function should take two terms of our calculus, and return a third.</li>
<li>(c)&nbsp; &nbsp;Predecessor

Repeat the above for a predecessor function over church numerals. This function should take one term of our calculus, and return another.</li>
</ol>
</div>
</div>
<div class="layoutArea"></div>
</div>
