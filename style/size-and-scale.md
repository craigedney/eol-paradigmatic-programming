
## Ratio-based scaling

```css
:root {
  --ratio: 1.5;
  --s-2: calc(var(--s-1) / var(--ratio));
  --s-1: calc(var(--s0) / var(--ratio));
  --s0: 1rem;
  --s1: calc(var(--s0) * var(--ratio));
  --s2: calc(var(--s1) * var(--ratio));
  --s3: calc(var(--s2) * var(--ratio));
  --s4: calc(var(--s3) * var(--ratio));
  --s5: calc(var(--s4) * var(--ratio));
}
```

## Viewport-width-based scaling with clamp

```css
:root {
  --s-2: clamp(0.78rem, calc(0.77rem + 0.03vw), 0.80rem);
  --s-1: clamp(0.94rem, calc(0.92rem + 0.11vw), 1.00rem);
  --s0: clamp(1.13rem, calc(1.08rem + 0.22vw), 1.25rem);
  --s1: clamp(1.35rem, calc(1.28rem + 0.37vw), 1.56rem);
  --s2: clamp(1.62rem, calc(1.50rem + 0.58vw), 1.95rem);
  --s3: clamp(1.94rem, calc(1.77rem + 0.87vw), 2.44rem);
  --s4: clamp(2.33rem, calc(2.08rem + 1.25vw), 3.05rem);
  --s5: clamp(2.80rem, calc(2.45rem + 1.77vw), 3.82rem);
}
```
