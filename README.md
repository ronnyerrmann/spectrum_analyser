# spectrum_analyser
Creates a Lomb-Scargle Periodogram

This was part of an job application exercise: A proprietary programm (WaveGen.exe) created some file containing a period signal. I had to find "the frequency of the highest amplitude wave in each file" and put it into a result file, together with the filename, and sort by frequency.

I have chosen the generalised Lomb-Scargle Periodogram to find the frequency of the highest amplitude.

Compile with a C++ compiler above version 11, e.g. [https://nuwen.net/mingw.htm](https://nuwen.net/mingw.htm)
```
g++ -o spectrum_analyser spectrum_analyser.cpp
```

The exe can either run in the folder with the files, or a the path to the files can be given.

The input CSV files need to have the following form (time or signal units can different):
```
Seconds,Volts
0, 0.3604565
4.00496E-07, 0.3604565
8.009919E-07, 0.3604565
...
3.604464E-06, 0.3604565
4.004959E-06, 0.3604565
4.405455E-06, -0.3604565
4.805951E-06, -0.3604565
5.206447E-06, -0.3604565
...
```

The code to save the Periodogram as .csv or to save the phase-folded signal as .csv is currently commented out.
