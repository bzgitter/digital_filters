# FIR LPF: As approximated from ideal filter
## Getting the ideal frequency response (Filter Spec.)
Filter design starts with stating your filter specification (Your Wish!). Ideally, LPF is expected to have the following frequency response

$$
H(\omega) = \begin{cases}
    e^{-j\omega \alpha} & \text{if } |\omega | \leq \omega _c \\
    0 & \text{otherwise}
\end{cases}
$$

Easy & Beautiful! But Imprcatical! (Says 'I need the signal below this cutoff ($\omega _$) frequency to 'pass without any problem' (see $H$ has magnitude 1) but rest not to pass at all! The signal can be phase shifted, LINEARLY ($-\omega\alpha$). DONT DO other change on my signal other than 'THIS', if any only a linear phase shift!)

The Practical Filter Spec. must include:
    <ul>
        <li> pass band ripple (tolerance?) $\delta _1 $ </li>
        <li> stop band ripple $\delta _2$ </li>
        <li> transition band  $\Delta \omega = \omega _s - \omega _c$ </li>
    <\ul>

## Getting the filter coefficients (The FIR!)

The inverse Fourier operator applied on the frequency respnse spec shall give the look of $h$, The Impulse Response! This becomes
$$
h(n) = sinc() = \omega _c\frac{sin(\omega _c (n-\alpha))}{\pi(n-\alpha)}
$$
## 