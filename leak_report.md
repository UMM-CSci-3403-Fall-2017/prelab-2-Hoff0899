# Leak report

The memory leaks are happening because the function creates a string to compare to the cleaned strings to the original string. The creation of this obviously takes up memory but this memory isn't being free'd after its use.

I will solve this by free'ing memory created by the creation of the compare string.
