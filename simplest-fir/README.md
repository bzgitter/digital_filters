# FIR LPF: As approximated from ideal filter
## Getting the ideal frequency response (Filter Spec.)
Filter design starts with stating your filter specification (Your Wish!). Ideally, LPF is expected to have the following frequency response

$$
\mathrm{CE}(p, y) = \begin{cases}
    1 & \text{if } |\sigma | \leq \sigma _c \\
    0 & \text{otherwise}
\end{cases}
$$

Easy & Beautiful! But Imprcatical! The Practical Filter Spec. must include:
\begin{itemize}
    \item pass band ripple (tolerance?) $\delta _1$
    \item stop band ripple $\delta _2$
    \item transition band  $\Delta \omega = \omega _s - \omega _c$
\end{itemize}
## Getting the filter coefficients (The FIR!)

The inverse Fourier operator applied on the frequency respnse spec shall give the look of $h$, impulse response
