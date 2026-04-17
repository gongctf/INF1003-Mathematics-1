# Argument
is a sequence of propositions/statements (True/False).

![{B903D603-F66B-46CF-85A4-045819943588}](attachments/{B903D603-F66B-46CF-85A4-045819943588}.png)  
**Premises** are statements/conditions that are assumed to be true to **imply a conclusion**.
- Premises are propositions that we assume are True.
**Conclusion** in a valid argument would only be true as long as all the premises really are true.
- Conclusion is what we can learn from assuming all the premises.

An argument is only valid if the premises really do imply the conclusion:

$$
Assumption_{1} \wedge Assumption_{2}\wedge\dots\to Conclusion\equiv True
$$


Example:  
Show that $a\wedge b\implies a\equiv True$

| a   | b   | $a\wedge b$ | $a\wedge b \implies a$ |
| --- | --- | ----------- | ---------------------- |
| T   | T   | T           | T                      |
| T   | F   | F           | T                      |
| F   | T   | F           | T                      |
| F   | F   | F           | T                      |
$a\wedge b\to a$ is a valid argument because the implication proposition is a tautology which can be seen from the truth table.

Example:

$$
\begin{gathered}
\forall x(Man(x)\implies Mortal(x)) \\
Man(Socrates) \\
\color{white} \rule{4cm}{0.4pt}\\
\therefore Mortal(Socrates)
\end{gathered}
$$

First 2 lines are premises, last line is conclusion

# Rules of inference
is a formula that can be used to build new arguments. Able to take known arguments or the argument form, and substitute generic premises with new premises.

## Modus Ponens
$$
\begin{gathered}
(p\wedge(p\implies q))\implies q \\
\\
p\\
p\implies q\\
\color{white} \rule{4cm}{0.4pt}\\
\therefore  q
\end{gathered}
$$

Example:  
Student declares "If it snows, then I will study Logic" $p\implies q$  
It is snowing $p$  
Conclusion: Therefore, Student will study logic $q$  
$(p\wedge(p\implies q))\implies q$ This argument will be valid if 2 of the premises were true.

## Modus Tollens
$$
\begin{gathered}
(\neg q\wedge(p\implies q))\implies \neg p\\
\\
\neg q\\
p\implies q\\
\color{white} \rule{4cm}{0.4pt}\\
\therefore  \neg p
\end{gathered}
$$

Example:  
Student declares "If it snows, then I will study Logic" $p\implies q$  
Student is not studying logic $\neg q$  
Conclusion: Therefore, "it is not snowing" $\neg p$

## Hypothetical Syllogism
$$
\begin{gathered}
((p\implies q)\wedge(q\implies r))\implies(p\implies r)\\
\\
p\implies q\\
q\implies r\\
\color{white} \rule{4cm}{0.4pt}\\
\therefore  q\implies r
\end{gathered}
$$

Example:  
Student declares "If it snows, then I will study Logic" $p\implies q$  
Student declares "If I study Logic, I will get an A" $q\implies r$  
Conclusion: "If it snows, I will get an A" $p\implies r$

## Disjunctive Syllogism
$$
\begin{gathered}
((p\vee q) \wedge \neg p) \implies q\\
\\
p\vee q\\
\neg p\\
\color{white} \rule{4cm}{0.4pt}\\
\therefore  q
\end{gathered}
$$

- If we know that "p or q" is true, and we know "p" is not true, then we conclude "q" is true because 1 of them must be true.

## Addition
$$
\begin{gathered}
p\implies(p\vee q)\\
\\
p\\
\color{white} \rule{4cm}{0.4pt}\\
\therefore  p\vee q
\end{gathered}
$$ 

If we know that something is true, then the conjunction of that with anything else is also true.

## Simplification
$$
\begin{gathered}
(p\wedge q)\implies p\\
\\
p\wedge q\\
\color{white} \rule{4cm}{0.4pt}\\
\therefore  p
\end{gathered}
$$

For a conjunction of 2 propositions to be true, each one of them has to be true.  
Example:  
Student declares "I will study logic and English Literature" $p\wedge q$  
Conclusion: Student will study logic $p$

## Conjunction
$$
\begin{gathered}
((p)\wedge(q))\implies(p\wedge q)\\
\\
p\\
q\\
\color{white} \rule{4cm}{0.4pt}\\
\therefore  p\wedge q
\end{gathered}
$$

## Resolution
$$
\begin{gathered}
((p\vee q)\wedge(\neg p\vee r))\implies(q\vee r)\\
\\
p\vee q\\
\neg p\vee r\\
\color{white} \rule{4cm}{0.4pt}\\
\therefore  q\vee r
\end{gathered}
$$

Looking at the premises, we have p in one of the disjunctions and not p in the other, but since both distinctions must be true, then at least in one of them r or q must be true, because in one of them the left hand side will be false.

Example:  
Let p be "I will study Logic"  
Let r be "I will study English literature"  
Let q be "I will study databases"

$\neg p\vee r$: "I will not study Logic or I will study English Literature"  
$p\vee q$: "I will study Logic or I will study databases"  
Conclusion: "I will study databases or I will study English Literature" $q\vee r$

## Examples
- Construct a valid argument for the conclusion: "If I do not finish writing the program, then i will wake up feeling refreshed"
	- Premises:
	- "If you send me an e-mail message, then I will finish writing the program" $p\implies q$
	- "If you do not send me an e-mail message, then I will go to sleep early" $\neg p\implies q$
	- "If I go to sleep early, then I will wake up feeling refreshed" $r\implies s$
	- Based on conclusion, we need to show $\neg q\implies s$
		- $p\implies q$  Premise 1
		- $\neg q\implies \neg p$ (Contrapositive of the above)
		- $\neg p\implies r$ Premise 2
		- $\neg q\implies r$ (Hypothetical Syllogism)
		- $r\implies s$ Premise 3
		- $\neg q\implies s$ (Hypothetical Syllogism)
		- This concludes our argument. 

# Rules of Inference in Predicate Logic
## Universal Instantiation
$$
\begin{gathered}
\forall xP(x)\\
\color{white} \rule{4cm}{0.4pt}\\
\therefore  P(c)
\end{gathered}
$$

Applying logic to specific cases based on general premises.

Example:
"All dogs are cuddly"
"Fido is a dog"
"Therefore, Fido is cuddly"
- The predicate p of x is true for every element in our universe, we conclude that the premise holds true for a specific element from the universe.

### Universal Modus Ponens
combines universal instantiation and modus ponens into one rule.

$$
\begin{gathered}
\forall x(P(x)\implies Q(x))\\
P(a) \text{ where a is an element in the domain}\\
\color{white} \rule{8cm}{0.4pt}\\
\therefore   Q(a)
\end{gathered}
$$

## Universal Generalisation
$$
\begin{gathered}
P(c) \text{ for an arbitrary c}\\
\color{white} \rule{4cm}{0.4pt}\\
\therefore  \forall xP(x)
\end{gathered}
$$

If you can show some property holds for an utterly random, unspecified member of a group. 

Example: Show "Everyone in the class can tie their shoes."
- Pick 1 person, call them "Alex", but you picked him as random and he is a completely ordinary, unspecified student.
- Alex ties their shoes using a general step-by-step tying method that would work for any student.
- Conclusion by UG: Since your argument didn't rely on any special facts about Alex, you can conclude "Everyone in the class can tie their shoes."

Example:  
"A triangle has 3 sides"  
- This statement refers to an arbitrary triangle, not a specific one
We can conclude that "every triangle has 3 sides"

Example:  
We assert that "A student in ICT knows programming"  
We conclude "All students in ICT possess programming knowledge"  

## Existential Instantiation
$$
\begin{gathered}
\exists xP(x)\\
\color{white} \rule{4cm}{0.4pt}\\
\therefore  P(c) \text{ for some element c}
\end{gathered}
$$

Example:  
If we know "Someone got an A", we can say  
"Let's call them x and state that x got an A"  
This lets us conclude the existence of such individuals within the group.

## Existential Generalisation
$$
\begin{gathered}
P(c) \text{ for some element c}\\
\color{white} \rule{4cm}{0.4pt}\\
\therefore  \exists xP(x)
\end{gathered}
$$

Example:  
"Michael got an A in the class"  
"Therefore, someone got an A in the class"

Example:  
"Fido the dog is cuddly"  
We conclude that some dogs are cuddly.

## Using Rules of Inference
Example: Using the rules of inference, construct a valid argument to show that  
"Johnny has a dream" is a consequence of the premises:  
"Every child has a dream." and "Johnny is a child."  
"Johnny has a dream" $Dream(Johnny)$  
"Every child has a dream" $\forall x(Child(x)\implies Dream(x))$  
"Johnny is a child" $Child(Johnny)$  

$$
\begin{gathered}
\forall x(Child(x)\implies Dream(x))\\
Child(Johnny)\\
\color{white} \rule{4cm}{0.4pt}\\
Dream(Johnny)
\end{gathered}
$$


| Step                                      | Reason                        |
| ----------------------------------------- | ----------------------------- |
| 1. $\forall x(Child(x)\implies Dream(x))$ | Premise                       |
| 2. $Child(Johnny)\implies Dream(Johnny)$  | UI from (1)                   |
| 3. Child(Johnny)                          | Premise                       |
| 4. Dream(Johnny)                          | Modus Ponens from (2) and (3) |

Example: Use rules of inference to prove Socrates is mortal

$$
\begin{gathered}
\forall x(Man(x)\implies Mortal(x))\\
Man(Socrates)\\
\color{white} \rule{4cm}{0.4pt}\\
\therefore  Mortal(Socrates)
\end{gathered}
$$

| Step                                         | Reason              |
| -------------------------------------------- | ------------------- |
| 1. $\forall x(Man(x)\implies Mortal(x))$     | Premise             |
| 2. $Man(Socrates) \implies Mortal(Socrates)$ | UI from (1)         |
| 3. Man(Socrates)                             | Premise             |
| 4. Mortal(Socrates)                          | MP from (2) and (3) |
