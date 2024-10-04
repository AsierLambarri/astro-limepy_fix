# astro-limepy_fix
Astro-limepy1.1 as of Oct 10, 2024, is only compatible with the earliest scipy releases: it uses *scipy.random* which was deprecated as early as in v1.0.0 in Oct 2017 and completely removed from the package in v1.3.0 (May 2019). Fruthermore it uses the function *scipy.integrate.simps*, which was renamed to *scipy.integrate.simpson* in v1.6.0 in Jan 2021. Furthermore, i found three issues with the code: the use of *is* statement in place of *==*, bad identation of line 850 of `spes.py` and bad seeding when generating samples. 

The changes made are the following:

* Changed 
