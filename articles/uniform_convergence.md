<!-- omit from toc -->
# Равномерная сходимость.

> Равномерная сходимость для функций нескольких переменнных, функциональных последовательностей и рядов. Критерий Коши равномерной сходимости. Определение равномерной сходимости по Гейне.

[[toc]]

## Равномерная сходимость функции нескольких переменных.

Пусть $ {D \subseteq \mathbb{R}^p} $, $ {E \subseteq \mathbb{R}^q} $ и множество $ E $ имеет предельную точку $ b $ (конечную или бесконечную). Функция $ {F (x, y) : D \times E \to \mathbb{R}^s} $, где $ x \in D $, $ y \in E $.

**Определение.** Говорят, что функция $ F(x, y) $ сходится **поточечно** по $ x $ на множестве $ D $ при $ y \to b $, если найдется такая функция $ \varphi : D \to \mathbb{R}^s $, что:

$$ \boxed{\forall x \in D} \ \ {\forall \varepsilon > 0} \ \ {\exists \overset{\circ}{U}_b} \ \ {\forall y \in \overset{\circ}{U}_b \cap E} \ \ {\| F(x, y) - \varphi(x) \| < \varepsilon}. $$

Что эквивалентно условию

$$ \forall x \in D \ \ \exists \lim_{y \to b} F(x, y) = \varphi(x). $$

**Определение.** Говорят, что функция $ F(x, y) $ сходится **равномерно** по $ x $ на множестве $ D $ при $ y \to b $, если найдется такая функция $ \varphi : D \to \mathbb{R}^s $, что:

$$ {\forall \varepsilon > 0} \ \ {\exists \overset{\circ}{U}_b} \ \ {\forall y \in \overset{\circ}{U}_b \cap E} \ \ \boxed{\forall x \in D} \ \ {\| F(x, y) - \varphi(x) \| < \varepsilon}. $$

Что эквивалентно существованию предела

$$ \lim_{y \to b} \sup_{x \in D} {\| F(x, y) - \varphi(x) \|} = 0. $$

Равномерная сходимость обозначается следующим образом:

$$ F(x, y) \overset{x \in D}{\underset{n \to \infty}{\rightrightarrows }} \varphi(x). $$

> Заметим, что из равномерной сходимости вытекает поточечная сходимость функции. Однако обратное неверно: поточечная сходимость не гарантирует равномерную сходимость.

## Равномерная сходимость функциональных последовательностей.

Если в качестве множества $ E $ в предыдущем определении мы рассмотрим множество натуральных чисел $ \mathbb{N} $, то положив $ f_n(x) = F(x, n) $ для всех $ x \in D $ и $ n \in \mathbb{N} $, получим определение равномерной сходимости для функциональных последовательностей.

**Определение.** Говорят, что функциональная последовательность $ f_n (x) $ сходится равномерно на множестве $ D $ при $ n \to \infty $, если найдется такая функция $ \varphi(x) : D \to \mathbb{R}^s $, что:

$$ {\forall \varepsilon > 0} \ \ {\exists n_0 \in \mathbb{N}} \ \ {\forall n \ge n_0} \ \ \boxed{\forall x \in D} \ \ {\| f_n (x) - \varphi(x) \| < \varepsilon}. $$

Это эквивалентно существованию предела

$$ \lim_{n \to \infty} \sup_{x \in D} {\| f_n (x) - \varphi(x) \|} = 0. $$

## Равномерная сходимость функциональных рядов.

Пусть имеется функциональная последовательность $ \{ f_n (x) \}_{n=1}^{\infty} $, где 

$$ {f_n : D \to \mathbb{R}}, \ \text{и} \ D \subseteq \mathbb{R}^p. $$

Пусть для всех $ x \in D $ сходится ряд

$$ \sum_{n=1}^{\infty} f_n (x). \tag{1} $$


**Определение.** Ряд $(1)$ cходиться равномерно на множестве $ D $, если

$$ {\sum_{n=1}^{m} f_n(x)} \ \overset{x \in D}{\underset{m \to \infty}{\rightrightarrows }} \ {\sum_{n=1}^{\infty} f_n (x)} $$


## Критерий Коши равномерной сходимости.

**Теорема.** (Критерий Коши равномерной сходимости)

Пусть выполнено следующее:

1. $ {D \subseteq \mathbb{R}^p} $, $ {E \subseteq \mathbb{R}^q} $ и множество $ E $ имеет предельную точку $ b $ (конечную или бесконечную).

2. Функция $ {F (x, y) : D \times E \to \mathbb{R}^s} $, где $ x \in D $, $ y \in E $.

В этом случае функция $ F(x, y) $ сходится равномерно в $ D $ при $ y \to b $ тогда и только тогда, когда верно:

$$ {\forall \varepsilon > 0} \ \ {\exists \overset{\circ}{U}_b} \ \ {\forall y_1, y_2 \in \overset{\circ}{U}_b \cap E} \ \ \boxed{\forall x \in D} \ \ {\| F(x, y_1) - F(x, y_2) \| < \varepsilon}. $$

**Доказательство:**

$ (\Rightarrow) $ Покажем необходимость условия Коши. 

Пусть верно условие теоремы и функция $ F(x, y) $ cходиться равномерно в $ D $ при $ y \to b $, тогда

$$\boxed{ {\forall \varepsilon > 0} \ \ {\exists \overset{\circ}{U}_b} \ \ {\forall y_1, y_2 \in \overset{\circ}{U}_b \cap E} \ \ {\forall x \in D} } $$

$$ {\| F(x, y_1) - \varphi(x) \| < \frac{\varepsilon}{2}} \ \ \text{,} \ \ {\| F(x, y_2) - \varphi(x) \| < \frac{\varepsilon}{2}}. $$

Из этого следует, что

$$ \| F(x, y_1) - F(x, y_2) \| \le \| F(x, y_1) - \varphi(x) \| + \| F(x, y_2) - \varphi(x) \| < \varepsilon. $$

Получим, что

$$ \boxed{\| F(x, y_1) - F(x, y_2) \| < \varepsilon} \ . $$

Значит для функции $ F(x, y) $ верно условие Коши.

$ (\Leftarrow) $ Покажем достаточность условия Коши.

Пусть для $ F(x, y) $ верно условие Коши равномерной сходимости. Тогда для $ F(x, y) $ верно и условие Коши поточечной сходимости функции, поэтому

$$ {\forall x \in D} \ {\exists \lim_{y \to b} F(x, y)}. $$

Положим, что $ \varphi(x) = {\lim_{y \to b} F(x, y)} $, для всех $ {x \in D} $.

Рассмотрим условие Коши равномерной сходимости функции:

$$ \boxed{{\forall \varepsilon > 0} \ \ {\exists \overset{\circ}{U}_b} \ \ {\forall y \in \overset{\circ}{U}_b \cap E} \ \ {\forall x \in D}} \ {\forall \widetilde{y} \in \overset{\circ}{U}_b \cap E} $$

$$ {\| F(x, y) - F(x, \widetilde{y}) \| < \frac{\varepsilon}{2}}. $$

Пользуясь непрерывностью нормы мы можем перейти в последнем неравенстве к пределу:

$$ {\lim_{\widetilde{y} \to b} \| F(x, y) - F(x, \widetilde{y}) \|} = {\| F(x, y) - \varphi(x) \|} \le \frac{\varepsilon}{2} < \varepsilon. $$

Получим, что:

$$ \boxed{{\| F(x, y) - \varphi(x) \|} < \varepsilon} \ . $$

Можем заключить, что функция $ F(x, y) $ сходиться равномерно в $ D $ при $ {y \to b} $.


## Определение равномерной сходимости по Гейне.

**Теорема.** (Равномерная сходимость по Гейне)

Функция $ F(x, y) $ сходиться равномерно в $ D $ при $ y \to b $ тогда и только тогда, когда для любой последовательности $ \{ y_n \}_{n=1}^{\infty} $ элементов из $ E $ такой, что $ y_n \ne b $ для всех $ n \in \mathbb{N} $ и $ y_n \to b $, верно, что функциональная последовательность $ \{ F(x, y_n) \}_{n=1}^{\infty} $ сходиться равномерно в $ D $.

$$ \exists \varphi(x) \ \forall \{ y_n \}_{n=1}^{\infty}, y_n \ne b, y \to b \ \ F(x, y_n) \overset{x \in D}{\underset{n \to \infty}{\rightrightarrows }} \varphi(x) $$