===========================================
輪読会 第19回
===========================================

3.3 スケーリング (p. 67)

補題 16
===============

(3.10)の導出について


.. math::
   :nowrap:

   \begin{align*}
   \mathbb{E}_w &= \frac{\int w \exp \left(-\frac{n\beta}{2}\left\| J^{1/2} \left(w - w_0 - \frac{\hat{\xi}_n}{\sqrt{n}} \right)\right\|^2 \right) dw}
   {\int \exp \left(-\frac{n\beta}{2}\left\| J^{1/2} \left(w - w_0 - \frac{\hat{\xi}_n}{\sqrt{n}} \right)\right\|^2 \right) dw} (1 + o_p(1))\\
   \text{分母} &= \int \exp \left(-\frac{n\beta}{2}\left\| J^{1/2} \left(w - w_0 - \frac{\hat{\xi}_n}{\sqrt{n}} \right)\right\|^2 \right) dw\\
   &= \left( \frac{2\pi}{n\beta} \right)^{d/2} \det (J)^{-1/2}
   \end{align*}

:math:`w - w_0 - \frac{\hat{\xi}_n}{\sqrt{n}} = A` とすると

.. math::
   :nowrap:

   \begin{align*}
   \text{分子} &= \int w \exp \left(-\frac{n\beta}{2}\left\| J^{1/2} \left(w - w_0 - \frac{\hat{\xi}_n}{\sqrt{n}} \right)\right\|^2 \right) dw\\
   &= \int (A + w_0 + \frac{\hat{\xi}_n}{\sqrt{n}}) \exp \left(-\frac{n\beta}{2}\left\| J^{1/2} \left(A \right)\right\|^2 \right) dw
   \end{align*}

奇関数は積分すると0になるので、

.. math::

   \text{分子} = \left(w_0 + \frac{\hat{\xi}_n}{\sqrt{n}}\right)\left( \frac{2\pi}{n\beta} \right)^{d/2} \det (J)^{-1/2}

したがって :math:`\mathbb{E}_w` は

.. math::
   :nowrap:

   \begin{align*}
   \mathbb{E}_w &= \left(w_0 + \frac{\hat{\xi}_n}{\sqrt{n}}\right)(1 + o_p(1))\\
   &= \left(w_0 + \frac{\hat{\xi}_n}{\sqrt{n}}\right) + \underbrace{o_p(1) + o_p(\frac{1}{\sqrt{n}})}_{収束が遅い方が残りそう??}\\
   &= \left(w_0 + \frac{\hat{\xi}_n}{\sqrt{n}}\right) + o_p(\frac{1}{\sqrt{n}}) \tag{3.10}
   \end{align*}


.. todo:: (3.10)の導出で :math:`o_p(1)` と :math:`o_p(\frac{1}{\sqrt{n}})` で小さい方が残るのは何故??
