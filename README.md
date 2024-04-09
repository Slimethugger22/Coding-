# Coding-
This is my coding store
\documentclass{article}
\usepackage{tikz}
\usetikzlibrary{shapes,arrows}

\begin{document}

\tikzstyle{startstop} = [rectangle, rounded corners, minimum width=3cm, minimum height=1cm,text centered, draw=black, fill=red!30]
\tikzstyle{io} = [trapezium, trapezium left angle=70, trapezium right angle=110, minimum width=3cm, minimum height=1cm, text centered, draw=black, fill=blue!30]
\tikzstyle{process} = [rectangle, minimum width=3cm, minimum height=1cm, text centered, draw=black, fill=orange!30]
\tikzstyle{decision} = [diamond, minimum width=3cm, minimum height=1cm, text centered, draw=black, fill=green!30]
\tikzstyle{arrow} = [thick,->,>=stealth]

\begin{tikzpicture}[node distance=2cm]

\node (start) [startstop] {Home Page};
\node (login) [io, below of=start] {Login};
\node (register) [process, below of=login] {Register};
\node (browse) [process, below of=register] {Browse Courses};
\node (profile) [process, below of=browse] {User Profile};
\node (search) [process, right of=browse, xshift=3cm] {Search Courses};
\node (enroll) [process, below of=search] {Enroll in Course};
\node (logout) [startstop, below of=enroll] {Logout};

\draw [arrow] (start) -- (login);
\draw [arrow] (login) -- (register);
\draw [arrow] (register) -- (browse);
\draw [arrow] (browse) -- (profile);
\draw [arrow] (browse) -- (search);
\draw [arrow] (search) -- (enroll);
\draw [arrow] (profile) -- (browse);
\draw [arrow] (enroll) -- (logout);

\end{tikzpicture}

\end{document}
