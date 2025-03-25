Replace these 3 files in sbitx 4.4 and you should getb performance improvements.
MWM AA2AY

1. Rationalize access to wisdom file
2. Usea single wisdom file instead of 2
3. Reuse plan files where possible insteadof recreating them each time
4. reuse buffer memory instead of freeing and reallocating it
5. Use FFTW to free memory(FFTW say this a must, if the memory is allocated with FFTW.
6. eliminate the use of modulo operator.(25 instruction cycles instead of 2 for compare)
7. In build file delete wisdom file when you compile.(recommended by FFTW developers)
8. Use fast math to speed up calculations
