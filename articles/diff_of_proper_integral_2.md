![](../imgs/headers/diff_of_proper_integral_2.svg)

<!-- omit from toc -->
# Непрерывность и дифференцируемость собственных интегралов с параметрами, когда пределы интегрирования зависят от параметров.

[[toc]]

## Непрерывность собственных интегралов с параметрами, когда пределы интегрирования зависят от параметров.

**Теорема.** О непрерывности собственных интегралов с параметрами, когда пределы интегрирования зависят от параметров.

Пусть дана функция $ f(x, y) : {[a, b] \times [c, d]} \to \mathbb{R} $. Также пусть имеются функции $ \alpha(y), \beta(y) $, определенные на $ [c, d] $, а их графики содержаться в $ [a, b] \times [c, d] $.

Функция $ f(x, y) $ непрерывна на $ [a, b] \times [c, d] $. Функции $ \alpha(y), \beta(y) $ непрерывны на $ [c, d] $.

Тогда функция $ \Phi(y) = \int_{\alpha(y)}^{\beta(y)} f(x, y) dx $ непрерывна на $ [c, d] $.

**Доказательство:**

Пусть $ y_0 \in [c, d] $. Покажем, что $ \exists \lim_{y \to y_0} \Phi(y) = \Phi(y_0) $.

$$ \Phi(y) = \int_{\alpha(y_0)}^{\beta(y_0)} f(x, y) dx + \int_{\alpha(y)}^{\alpha(y_0)} f(x, y) dx - \int_{\beta(y)}^{\beta(y_0)} f(x, y) dx. $$

Заметим, что по теореме [о непрерывности собственных интегралов с параметрами](./limits_of_proper_integral.md) интеграл $ \int_{\alpha(y_0)}^{\beta(y_0)} f(x, y) dx $ является непрерывной в точке $ y_0 $ функцией. 

Поэтому для доказательства теоремы, достаточно показать, что интегралы $ \int_{\alpha(y)}^{\alpha(y_0)} f(x, y) dx $ и $ \int_{\beta(y)}^{\beta(y_0)} f(x, y) dx $ являются непрерывными по $ y $ функциями в точке $ y_0 $.

$$ 0 \le \left| \int_{\alpha(y)}^{\alpha(y_0)} f(x, y) dx - \underbrace{\int_{\alpha(y_0)}^{\alpha(y_0)} f(x, y_0) dx}_{=0}  \right| = \left| \int_{\alpha(y)}^{\alpha(y_0)} f(x, y) dx \right| \le $$

$$ \left| \int_{\alpha(y)}^{\alpha(y_0)} \left| f(x, y) \right| dx \right| \le \left| \int_{\alpha(y)}^{\alpha(y_0)} \max_{(x, y) \in [a, b] \times [c, d]} \left| f(x, y) \right| dx \right| = $$

$$ = \left| \alpha(y_0) - \alpha(y) \right| \max_{(x, y) \in [a, b] \times [c, d]} \left| f(x, y) \right| \underset{y \to y_0}{\longrightarrow} 0. $$

Заметим, что по теореме Вейерштрасса максимум достигается, т.к. $ f(x, y) $ непрерывна на компактном множестве $ [a, b] \times [c, d] $.

Получим, что функция $ \int_{\alpha(y)}^{\alpha(y_0)} f(x, y) dx $ непрерывна в $ y_0 $. 

Для $ \int_{\beta(y)}^{\beta(y_0)} f(x, y) dx $ доказательство аналогичное.

Теорема доказана.

$$  $$

## Дифференцируемость собственных интегралов с параметрами, когда пределы интегрирования зависят от параметров.

**Теорема.** О дифференцируемости собственных интегралов с параметрами, когда пределы интегрирования зависят от параметров.

Пусть дана функция $ f(x, y) : {[a, b] \times [c, d]} \to \mathbb{R} $. Также пусть имеются функции $ \alpha(y), \beta(y) $, определенные на $ [c, d] $, а их графики содержаться в $ [a, b] \times [c, d] $.

Также пусть выполнено следующее:

1. $ f(x, y) $ непрерывна на $ [a, b] \times [c, d] $;

2. $ f^{\prime}_y (x, y) $ существует и непрерывна на $ [a, b] \times [c, d] $;

3. $ \alpha(y), \beta(y) $ дифференцируемы на интервале $ [c, d] $.

Тогда для $ \Phi(y) = \int_{\alpha(y)}^{\beta(y)} f(x, y) dx $ верно, что

$$ \forall y \in [c, d] \ \ \exists \Phi^{\prime} (y) = \int_{\alpha(y)}^{\beta(y)} f^{\prime}_y (x, y) dx + \beta^{\prime}(y) f(\beta(y), y) - \alpha^{\prime}(y) f(\alpha(y), y). $$

**Доказательство:**

Пусть $ y_0 \in [c, d] $.

$$ \Phi(y) = \int_{\alpha(y_0)}^{\beta(y_0)} f(x, y) dx + \int_{\beta(y_0)}^{\beta(y)} f(x, y) dx - \int_{\alpha(y_0)}^{\alpha(y)} f(x, y) dx. $$

По [теореме о дифференцировании собственных интегралов с параметрами](./diff_of_proper_integral_1.md)

$$ \exists \left. \frac{d}{dy} \int_{\alpha(y_0)}^{\beta(y_0)} f(x, y) dx \ \right|_{y=y_0} = \int_{\alpha(y_0)}^{\beta(y_0)} f^{\prime}_y (x, y_0) dx. $$

Поэтому для доказательства теоремы достаточно показать, что

$$ \left. \frac{d}{dy} \int_{\beta(y_0)}^{\beta(y)} f(x, y) dx \ \right|_{y=y_0} \overset{?}{=} \beta^{\prime}(y_0) f(\beta(y_0), y_0). $$

Для этого запишем левую часть равенства через предел

$$ \lim_{y \to y_0} \frac{1}{y - y_0} \left[ \int_{\beta(y_0)}^{\beta(y)} f(x, y) dx - \underbrace{\int_{\beta(y_0)}^{\beta(y)} f(x, y) dx }_{=0} \right] = $$

$$ = \lim_{y \to y_0} \frac{1}{y - y_0} \int_{\beta(y_0)}^{\beta(y)} f(x, y) dx. \tag{1} $$

По теореме функция $ \int_{\beta(y_0)}^{\beta(y)} f(x, y) dx $ непрерывна на интервале $ [c, d] $, поэтому в силу первой теоремы о среднем

$$ \forall y \in [c, d] \ \ \exists \xi_y \in [\min \{ \beta(y), \beta(y_0) \}, \max \{ \beta(y), \beta(y_0) \}] $$

$$ \int_{\beta(y_0)}^{\beta(y)} f(x, y) dx = f(\xi_y, y) (\beta(y) - \beta(y_0)). $$

Продолжим равенство $ (1) $

$$ \lim_{y \to y_0} \frac{1}{y - y_0} \int_{\beta(y_0)}^{\beta(y)} f(x, y) dx = \lim_{y \to y_0} \frac{\beta(y) - \beta(y_0)}{y - y_0} f(\xi_y, y) = $$

$$ = \beta^{\prime}(y_0) f(\beta(y_0), y_0). $$

Равенство $ \overset{?}{=} $ доказано.

Для $ \int_{\alpha(y_0)}^{\alpha(y)} f(x, y) dx $ доказательство аналогичное.