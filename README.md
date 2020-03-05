# ConUCSSEThesis
A repo containing useful thesis packages

## makexRef
`conucssethesis.sty` corrently contains `makexRef` to allow one to simple make optimal references with minimal typing. The following referenes are defined already:
````latex
\makexRef{xf}{Figure}{Figures}
\makexRef{xt}{Table}{Tables}
\makexRef{xe}{Equation}{Equations}
\makexRef{xth}{Theorem}{Theorems}
````

This allows us to reference one or more figures, as in the following example:
````latex
\begin{figure}
    \caption{Caption}
    \label{fig:mylabel}
\end{figure}
\begin{figure}
    \caption{Caption}
    \label{fig:mylabelA}
\end{figure}
\begin{figure}
    \caption{Caption}
    \label{fig:mylabelB}
\end{figure}
````
One at a time `\xf{fig:mylabelB}` yielding:
````
Figure 3
````
Two of them `\xf{fig:mylabelB, fig:mylabelA}`
````
Figure 3 and 2
````
Or any number `\xf{fig:mylabel, fig:mylabelA, fig:mylabelB}`
````
Figures 1, 2 and 3
````

This cross-referencing scheme can be overwritten by using the same command-sequence in the first parameter of makexRef, with the second and third parameters simply being the singular and plural form to prefix with.

