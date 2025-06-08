\documentclass{pssbmac}

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%% POR FAVOR, NÃO FAÇA MUDANÇAS NESSE PADRÃO QUE ACARRETEM  EM
%% ALTERAÇÃO NA FORMATAÇÃO FINAL DO TEXTO
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% POR FAVOR, ESCOLHA CONFORME O CASO
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\usepackage[brazil]{babel} % texto em Português
%\usepackage[english]{babel} % texto em Inglês

%\usepackage[latin1]{inputenc} % acentuação em Português ISO-8859-1
\usepackage[utf8]{inputenc} % acentuação em Português UTF-8
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%% POR FAVOR, NÃO ALTERAR
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\usepackage{qrcode}
\usepackage[spanish]{babel}
\usepackage[left=2.5cm,right=2.5cm,top=2.5cm,bottom=2.5cm]{geometry}
\usepackage{xurl}
\usepackage{cancel}
\usepackage[utf8]{inputenc} 
\usepackage[T1]{fontenc}
\usepackage{float}
\usepackage{graphics}
\usepackage{graphicx}
\usepackage{epsfig}
\usepackage{indentfirst}
\usepackage{amsmath, amsfonts, amssymb, amsthm, mathtools}
\usepackage{url}
\usepackage{csquotes}
% Ambientes pré-definidos
\newtheorem{theorem}{Theorem}[section]
\newtheorem{lemma}{Lemma}[section]
\newtheorem{proposition}{Proposition}[section]
\newtheorem{definition}{Definition}[section]
\newtheorem{remark}{Remark}[section]
\newtheorem{corollary}{Corollary}[section]
\newtheorem{teorema}{Teorema}[section]
\newtheorem{lema}{Lema}[section]
\newtheorem{prop}{Proposi\c{c}\~ao}[section]
\newtheorem{defi}{Defini\c{c}\~ao}[section]
\newtheorem{obs}{Observa\c{c}\~ao}[section]
\newtheorem{cor}{Corol\'ario}[section]

% ref bibliográficas
\usepackage[backend=biber, style=numeric-comp, maxnames=50]{biblatex}
\addbibresource{refs.bib}
\DeclareTextFontCommand{\emph}{\boldmath\bfseries}
\DefineBibliographyStrings{brazil}{phdthesis = {Tese de doutorado}}
\DefineBibliographyStrings{brazil}{mathesis = {Disserta\c{c}\~{a}o de mestrado}}
\DefineBibliographyStrings{english}{mathesis = {Master dissertation}}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\usepackage[utf8]{inputenc} 
\begin{document} 
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% TÍTULO E AUTORAS(ES)
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\title{DEDUCCIÓN DE LAS CONDICIONES DEL MÉTODO DE VARIACIÓN DE PARAMETROS DE SEGUNDO ORDEN CON APLICACIÓN}

\author{
    {\large Soberanes Gómez Erick Misdiel}\\
    {\small ESCUELA SUPERIOR DE INGENIERIA Y ARQUITECTURA} \\
    {\large Ecuaciones Diferenciales} \\
    {\small Junio 2, 2025} \\
}
\criartitulo
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% TEXTO
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\section{INTRODUCCIÓN}

El método de variación de parámetros constituye un instrumento analítico de suma relevancia para comprender la solución particular de ecuaciones diferenciales lineales no homogéneas.  Dicho método, al partir de las soluciones fundamentales de la ecuación homogénea asociada, permite la construccion de una solución particular mediante la introducción de funciones auxiliares que modulan las constantes presentes en la solución general de la ecuación homogénea.
No unicamente depende de la forma especifica del termino no homogeneo,emerge como la herramienta en la resolucion de problemas dinamicos en varias disciplinas en donde la aplicacion de los metodos requiere ser precisos y flexibles.


\section{ANÁLISIS MATEMÁTICO}


 A partir de la siguiente forma (Segundo Orden) la solucion que proporcionara que satisfaga el metodo de variacion de parametros:
\[y^{(2)} + p(x)y= q(x)\]

Se reconstruira al final de la siguiente forma de:
\[y(x) = y_h(x) + y_p(x)\]
donde:
\[y_h(x)=c_1y_1 + c_2y_2\]
\[ y_p(x)=c_1(x)y_1 + c_2(x)y_2\]
es decir:
\[y(x) = y_h + y_p = c_1y_1 + c_2y_2 + c_1(x)y_1 + c_2(x)y_2\]

Una vez formulada , se debe realizar una ecuacion de este tipo, encontrando la ecuacion homogenea relacionada, se da a buscar las dos soluciones linealmente independientes , en donde no sean multiplos de $ y_1(x), y_2(x)$ una de la otra y en donde $c_1 , c_2$ son constantes arbitrarias.

\[y_h = c_1y_1 +  c_2y_2\]
La meta a alcanzar con este metodo es encontrar la solucion particular que cuente con la misma forma que la solucion homogenea ,pero a cambio de las constantes homogeneas, sea funciones que no tenga una solucion por el momento.
Por ahora, nos conformaremos con que la solucion homogenea se tome con valor de CERO y que las funciones a determinar sean $c_1, c_2.$ \newline

\[y^{(2)} + p(x)y= 0\]

\section{PROCEDIMIENTO}
\emph{PASO 1} Debemos tener en cuenta que al obtener la solucion homogenea , lo unico que nos falta en derivar en dos ocasiones ,ya que en la ecuacion original es de segundo orden. 
\[y_p(x) = c_1y_1 +  c_2y_2\]
Primera derivada:
\[y_p^{(1)} = c_1y_1^{(1)} +c_1^{(1)}y_1 + c_2y_2^{(1)}+c_2^{(1)}y_2\]
Nota:comenzamos con 4 soluciones lineales independientes\\\\\\
Para ahora, incluir la Segunda derivada:

\[y_p^{(2)} = c_1^{(2)}y_1 +c_1^{(1)}y_1^{(1)}+c_1^{(1)}y_1^{(1)}+c_1y_1^{(2)}+c_2^{(2)}y_2+
c_2^{(1)}y_2^{(1)} +c_2^{(1)}y_2^{(1)}+c_2y_2^{(2)}\]
Nota:ahora cuenta con 8 soluciones lineales independientes\\\\

\emph{PASO 2} A partir de lo anterior se sustituira en la ecuacion original de segundo orden: 
\[y_p^{(2)} + p(x)y_p= q(x)\]
Sustituyendo:
\begin{equation}
(c_1^{(2)}y_1 +c_1^{(1)}y_1^{(1)}+c_1^{(1)}y_1^{(1)}+c_1y_1^{(2)}+c_2^{(2)}y_2+
c_2^{(1)}y_2^{(1)} +c_2^{(1)}y_2^{(1)}+c_2y_2^{(2)})+p(x)(c_1y_1+c_2y_2)=q(x)
\end{equation}
Nota:ahora cuenta con 10 soluciones lineales independientes\\\\\\
\emph{PASO 3} Se impone una condicion que nos reduzca terminos
\[c_1^{(1)}y_1 +c_2^{(1)}y_2  =0\]
Se deriva la condicion:
\[c_1^{(2)}y_1+c_1^{(1)}y_1^{(1)} +c_2^{(2)}y_2+c_2^{(1)}y_2^{(1)}  =0\]
\emph{PASO 4} Ahora ,se sustituira la condicion derivada para poder simplificar terminos:\\\
*Sustituyendo la condicion de (1)
\usepackage{\xcancel}
\[(\xcancel{c_1^{(2)}y_1}+\xcancel{c_1^{(1)}y_1^{(1)}}+c_1^{(1)}y_1^{(1)}+c_1y_1^{(2)}+\xcancel{c_2^{(2)}y_2}+\xcancel{c_2^{(1)}y_2^{(1)}}
 +c_2^{(1)}y_2^{(1)}+c_2y_2^{(2)})+p(x)(c_1y_1+c_2y_2)=q(x)\]
\[\cancel{c_1^{(2)}y_1}+\cancel{c_1^{(1)}y_1^{(1)} }+\cancel{c_2^{(2)}y_2}+\cancel{c_2^{(1)}y_2^{(1)}}\]
RESTANTE:
\[c_1^{(1)}y_1^{(1)}+c_1y_1^{(2)}+c_2^{(1)}y_2^{(1)}+c_2y_2^{(2)})+p(x)(c_1y_1+c_2y_2)=q(x)\]
\[10-4=6=q\]
Nota:ahora cuenta con 6 soluciones lineales independientes\\\\

\emph{PASO 5} Posteriormente, se factoriza por termino comun $c_1,c_2$
\begin{equation}
c_1(y_1^{(2)} +p(x)y_1)+c_2(y_2^{(2)}+p(x)y_2)+c_1^{(1)}y_1^{(1)}+c_2^{(1)}y_2^{(1)}=q(x)
\end{equation}
\emph{PASO 6} Para recordar , que $y_1, y_2$ son soluciones homogeneas y parte de el conjunto fundamental de soluciones
\[y_1^{(2)} +p(x)y _1=0\]; \[y_2^{(2)} +p(x)y _2=0\]
Aplicando estas condiciones en la ecuación (2), nos queda:
\[\cancel{c_1(y_1^{(2)} +p(x)y_1})+\cancel{c_2(y_2^{(2)}+p(x)y_2)}+c_1^{(1)}y_1^{(1)}+c_2^{(1)}y_2^{(1)}=q(x)\]
\[\cancel{y_1^{(2)} +p(x)y _1}\]; \[\cancel{y_2^{(2)} +p(x)y _2}\]\
\[6-4=2=q\]
RESTANTE:
\[c_1^{(1)}y_1^{(1)}+c_2^{(1)}y_2^{(1)}=q(x)\]
\emph{PASO 7}  De tal forma que construiremos un sistema de ecuaciones con la solución homogenea y particular para obtener las variables $c_1, c_2$ 
\[
\begin{cases}
c_1 y_1 + c_2 y_2 = 0 \\
c_1' y_1' + c_2' y_2' = q(x)
\end{cases}
\]

\emph{PASO 8} De tal modo, que lo único que nos queda es reconstruir la solución general:

\[y(x) = y_h+y_p\]
en donde recordaremos que consiste en la suma de la solución homogénea y una solución particular.\\\\\\

\section{APLICACIÓN AL MÉTODO DE  VARIACIÓN DE PARAMETROS}

\section*{1. Ecuación Diferencial no Homogénea}

Consideramos ahora la ecuación no homogénea:

\begin{equation}
    y'' - 3y' + 2y = e^t
\end{equation}
Es una ecuación con coeficientes constantes. Su forma característica es:

\begin{equation}
    m^2 - 3m + 2 = 0
\end{equation}

Resolviendo:

\begin{equation}
    (m - 1)(m - 2) = 0 \Rightarrow m_1 = 1, \quad m_2 = 2
\end{equation}
\section*{2. Solución homogénea}
Usaremos el método de variación de parámetros. Sean:

\[
y_1(t) = e^t, \quad y_2(t) = e^{2t}
\]
Por tanto, la solución general de la ecuación homogénea es:

\begin{equation}
    y_h(t) = C_1 e^t + C_2 e^{2t}
\end{equation}
Buscamos una solución particular de la forma:

\begin{equation}
    y_p(t) = u_1(t) y_1(t) + u_2(t) y_2(t)
\end{equation}

\section*{3.Condiciones de variación de parametros de orden 2}

El sistema a resolver es:

\[
\begin{cases}
u_1(t) y_1(t) + u_2(t) y_2(t) = 0 \\
u_1'(t) y_1'(t) + u_2'(t) y_2'(t) = q(t)
\end{cases}
\]

donde \( q(t) = e^t \). Sustituyendo:

\[
\begin{cases}
u_1(t) e^t + u_2(t) e^{2t} = 0 \\
u_1'(t) e^t + u_2'(t) \cdot 2e^{2t} = e^t
\end{cases}
\]

Restando la primera ecuación de la segunda:

\begin{equation}
    u_2'(t) e^{2t} = e^t \Rightarrow u_2'(t) = e^{-t} \Rightarrow u_2(t) = -e^{-t}
\end{equation}

Sustituyendo en la primera ecuación:

\begin{equation}
    u_1'(t) e^t + e^{-t} e^{2t} = 0 \Rightarrow u_1'(t) = -1 \Rightarrow u_1(t) = -t
\end{equation}

\section*{4. Solución Particular}

\begin{equation}
    y_p(t) = u_1(t) y_1(t) + u_2(t) y_2(t) = -t e^t - e^t
\end{equation}

\section*{5. Solución General}

La solución general de la ecuación no homogénea es:

\begin{align}
    y(t) &= y_h(t) + y_p(t) \nonumber \\
         &= C_1 e^t + C_2 e^{2t} - t e^t - e^t \nonumber \\
         &= (C_1 - 1)e^t + C_2 e^{2t} - t e^t
\end{align}



Dado que las soluciones son linealmente independientes y el método es válido.

\section{CONCLUSIÓN}
Con este tipo de ecuaciones otorgadas ,puedes llegar un resultado satisfaga a cualquier ecuacion diferencial de forma lineal no homogenea. Aunque,dicho metodo, lejos de ser un atajo, es la muestra clara que gana flexibilidad que siginfica que hay que aceptar mas estructuras para lograr variar los parametros. Esta etapa es crucial, ya, proporciona la estructura sobre la cual se agregara,para posteriormente, la solucion particular correspondente a la parte no homogenea.
El dominio de este proceso no solo facilita la compresion de la teoria , sino que tambien permitira abordar con eficacia a una variedad de problemas matematicos y fisicos mediante ecuaciones. \\\\\\\\\\\\   
\section{REFERENCIAS BIBLOGRAFICAS}
\newcommand{\urlfontsize}{\footnotesize} 

\begin{enumerate}


    \item Apuntes de Ecuaciones Diferenciales. ESCOM (pag. 145-147). \\ 
 
\url{https://www.escom.ipn.mx/docs/oferta/matDidacticoISC2009/EDfrncls/Apuntes_EcuDiferenciales_o3.pdf}
    
    \item Método de Variación de Parámetros. Canek - UAM. \\ 
   
    \ \url{http://canek.uam.mx/Ecuaciones/Teoria/4.LinealesOrdenSuperior/impVariacion.pdf}
    
    \item Method of variation of parameters. ecampusontario. \\ 
   

    \url{https://ecampusontario.pressbooks.pub/diffeq/chapter/3-5-method-of-variation-of-parameters/}
\end{enumerate}

\section{CODIGO LATEX}

 \qrcode[height=5cm]{https://ecampusontario.pressbooks.pub/diffeq/chapter/3-5-method-of-variation-of-parameters/}

\end{document}

\end{document}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% REFS BIBLIOGRÁFICAS
% POR FAVOR, NÃO ALTERAR
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\printbibliography
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\end{document}
