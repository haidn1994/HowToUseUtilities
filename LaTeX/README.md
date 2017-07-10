# LaTeX?

수학, 물리, 통계와 같이 수식이 많이 등장하는 주제에 대해서 전자문서로 정리하고 관리하려면 그에 걸맞는 툴이 필요하다.  
그런 역할을 훌륭하게 수행할 수 있는 프로그램은 바로 LaTeX이다.  

```{.tex}
    \documentclass[12pt]{article}
    \usepackage[utf8]{amsmath}

    \title{First LaTeX-doc}
    \author{haidn1994 }
    \date{July 2017}

    \begin{document}
	\maketitle
	\LaTeX{} is a document preparation system for the \TeX{}
typesetting program. It offers programmable desktop publishing features and extensive facilities for automating most aspects of typesetting desktop publishing, including numbering and cross-referencing, table and figures, page layout, and much more. \LaTeX{} was originally written in 1984 by Leslie Lamport and has become the dominant method for using \TeX{}; few people write in plain \TeX{} anymore. The current version is \LaTeXe

    \begin{align}
    E &= mc^2           				   \\
    m &= \frac{m_0}{\sqrt{1-\frac{v^2}{c^2}}}
    \end{align}
	 \section{Introduction}


    \end{document}
```

인터넷에 돌아다니는 가장 간단한 예제다.  
이걸 온라인 LaTeX에 붙여넣고 컴파일하면 굉장히 미려한 문서를 얻을 수 있다는 사실을 알 수 있을 것이다.  
이제 하나씩 차근차근 명령어를 알아보자.

## 기본적인 명령어

먼저 예약된 특수문자들을 알아보자.

> \{ \}, \[ \], \#, %, \\, &, \-, \_

등이 있다. \[\]나 \{\}에는 파라미터가 들어간다.  
% 우측으로는 주석문을 작성하는데 사용한다.  
\-가 연속으로 세개 있으면 긴 대시를 표현할 수 있다.  
문단은 빈줄 하나 이상으로 표현한다. 단어는 띄어쓰기 하나 이상으로 구분한다.  


모든 LaTeX명령어는 \\으로 시작한다.  
여기서 가장 중요한 명령어 3개를 소개한다.

> \\begin\{document\}, \\end\{document\}, \\documentclass\{\}

TeX문서는 모두 \\begin\{document\}로 시작해서 \\end\{document\}로 끝난다.  
\\end\{document\}뒤에는 모두 무시된다. 이 두 명령어 사이를 본문이라 한다.  
그리고 본문전에 필요한 모든 코드, 사항들을 전처리부(preamble)이라한다.  

## 기본적인 documentclass와 옵션

1. article
	* 논문, 짧은 문서나 출판물 속에 들어갈 기사와 같은 것에 어울린다. 
2. report
	* 좀 더 기술적인 문서 작성에 알맞다. 이는 chapter를 가지며 제목을 별도의 페이지에 인쇄하는 점을 제외하면 article과 같다.
3. book
	* 책자의 출판을 목적으로 한다. 종이의 양면에 인쇄할 것으로 가정하여 페이지의 구성을 조정한다.
4. 11pt
	* 일반적으로 사용하는 10포인트 말고 11포인트로 한다. 10포인트에 비해 10퍼센트 가량 크다.
5. 12pt
	* 10포인트에 비해 20퍼센트 정도 크다.

## 수학 기호

1. 지수와 첨자는 \_와 ^로 표기한다. 예를 들어 x\_\{1\} = p&\{\}와 같이 사용한다.
