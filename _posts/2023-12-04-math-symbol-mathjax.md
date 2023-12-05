---
title: "Mathematics blogging with mathjax"
categories: [posts]
tags: [mathjax]
last_modified_at: 2023-12-05
---



# Org-mode Markdown Preview

-   [X] Org-mode 기준 - 제킬 블로그로 내보내기 되어야 함
-   [X] latex 패키지 부담 없이 심플하게 프리퓨까지 커버
-   [X] Markdown 에서도 동일한 수식 표기 입력
-   [X] notes / blogs md 내보내기 검증 - mathjax 켜라!

mathjax 로 Org-mode 와 Markdown 을 커버한다. Typst 는 호환이 안되는것 같다. 굳이 그럴 필요 없다.

-   [MathJax로 LaTeX 사용하기 - 기계인간 John Grib - johngrib.github.io](https://johngrib.github.io/wiki/mathjax-latex/)
-   <https://tyami.github.io/blog/practice-for-mathjax/>


# Org mode with Math fragments



Org mode can contain LaTeX math fragments, and it supports ways to process these for several export back-ends. When exporting to LaTeX, the code is left as it is. When exporting to HTML, Org can use either MathJax (see Math formatting in HTML export) or transcode the math into images (see Previewing LaTeX fragments).

조직 모드에는 LaTeX 수학 조각이 포함될 수 있으며, 여러 내보내기 백엔드에서 이러한 조각을 처리하는 방법을 지원합니다. LaTeX 로 내보낼 때는 코드가 그대로 남습니다. HTML 로 내보낼 때 Org 는 MathJax 를 사용하거나(HTML 내보내기의 수학 서식 참조) 수학을 이미지로 트랜스코딩할 수 있습니다(LaTeX 조각 미리 보기 참조).

<https://orgmode.org/manual/LaTeX-fragments.html>


# math-preview with mathjax



샘플 존그립님


## 표기법: 조합

-   조합을 의미하는 Combination 을 다음과 같이 괄호를 써서 위아래로 표기하고, 이항 계수라 부른다.
-   의미는 똑같지만 $$aCb$$ 는 $$a \times C \times b$$로 착각하기 좋은 모양이라 $$\binom{a}{b}$$를 선호한다.

$$

\begin{align}
a C b & = \binom{a}{b} \\
3 C 2 & = \binom{3}{2} = 3 \\
\end{align}

$$


## 이항 정리

****Binomial Theorem****

$$

\begin{align}
(x+y)^n & = \sum_{j=0}^n \binom{n}{j} x^{n-j} y^j \\
    & = \binom{n}{0} x^{n} y^0
        + \binom{n}{1} x^{n-1} y^1
        + ...
        + \binom{n}{n-1} x^{1} y^{n-1}
        + \binom{n}{n} x^{0} y^{n} \\
\end{align}

$$

중학교 때 배운 곱셈 공식을 생각해 볼 수 있을 것이다.

$$(a+b)^2 = a^2 + 2ab + b^2$$

이 등식의 계수는 왜 $$1, 2, 1$$ 이 될까?

식을 전개하는 과정이 a 와 b 가 들어있는 주머니에서 중복을 무시하고 2 번 꺼내서 나열하는 것과 같기 때문이다.

$$

\begin{array}{rlllllllll}
(a+b)^2 & = & a^2 & + & 2ab & + & b^2 \\
        &   & aa  &   & ab  &   & bb  \\
        &   &     &   & bb  &   &     \\
\end{array}

$$

$$(a+b)^3$$ 형태도 마찬가지다.

$$

\begin{array}{rlllllllll}
(a+b)^3 & = & a^3 & + & 3a^2b & + & 3ab^2 & + & b^3 \\
        &   & aaa &   & aab   &   & bba   &   & bbb \\
        &   &     &   & aba   &   & bab   &   &     \\
        &   &     &   & baa   &   & abb   &   &     \\
\end{array}

$$

즉, $$ (a+b)^n $$ 형태의 각 항의 계수는 조합 $$\binom{n}{k}$$ 형태로 표현할 수 있다.
