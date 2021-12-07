===============================================================================
ExoMol molecular line lists -- XLII: 
Rovibronic molecular line list for the low-lying states of NO

Qianwei Qu, Sergei N. Yurchenko, and Jonathan Tennyson
MNRAS 2021


An accurate line list, called XABC, is computed for nitric oxide which covers 
its pure rotational, vibrational and rovibronic spectra. A mixture of empirical 
and theoretical electronic transition dipole moments are used for the final 
calculation of 14N16O rovibronic transitions belong to the A2Sigma+ -- X2Pi, 
B2Pi -- X2Pi and C2Pi -- X2Pi which correspond to the gamma, beta and delta 
band systems, respectively, as well as  minor improvements to transitions 
within the X2Pi ground state. The work is a major update of the ExoMol NOname 
line list. It provides a high-accuracy NO ultraviolet line list covering the 
complicated regions where the B-C states interact. XABC provides comprehensive 
data for the lowest four doublet states of NO in the region of the wavelength 
is longer than 160 nm (wavenumber < 63000 cm-1) for the analysis of atmospheric
NO on Earth, Venus or Mars,  other astronomical observations and applications.


Description: 

The states file .states contains lists of rovibronic states. Each state is labelled 
with the total angular momentum, state degeneracy,  total parity, vibrational 
quantum number, projection of the electronic, spin and total angular momenta. 
Each state has a unique number, which is the number of the row in which it 
appears in the file. This number is the means by which the state is related 
to the second part of the data system, the transitions files. The lifetimes 
and Lande-g factors are also provided. 

The transition file .trans contains four columns: the reference number in the 
energy file of the upper state, that of the lower state, the Einstein A 
coefficient of the transition and the transition wavenumber. These entries 
are ordered by increasing frequency. 

The .pf files contain the partition function (0...5000 K) tabulated 
in steps of 1 K. The pf_param.dat contains unitless expansion parameters 

Byte-by-byte description of file: .trans
-------------------------------------------------------------------------------
  Bytes   Format   Units   Label  Explanations
-------------------------------------------------------------------------------
  1 - 12   I12     ---     i'    Upper state ID
 13 - 25   I13     ---     i"    Lower state ID
 26 - 37   E12.4   s-1     A     Einstein A-coefficient of the transition
 38 - 53   f16.6   cm-1    nu    Transition wavenumber
-------------------------------------------------------------------------------

Byte-by-byte description of the states file: .states 
-------------------------------------------------------------------------------
  Bytes Format Units   Label  Explanations
-------------------------------------------------------------------------------
   1- 12  i12   ---   N             State ID, non-negative integer index
  13- 27  f15.6 cm-1  E             State energy term value in cm-1
  28- 34  i7    ---   g             Total state degeneracy
  35- 42  f8.1  ---   J             [0/184.5] J-quantum number, the total angular
                                    momentum excluding nuclear spin
  43- 55  f13.6 cm-1  Delta E       Energy uncertainty in cm-1
  56- 68  e13.4 s-1   tau           Life time
  69- 78  f10.6  ---   g             Lande g-factor
  79- 82  a4    ---   +/-           Total parity
  83- 86  a4    ---   e/f           Rotationless-parity
  87- 96  a10   ---   State         Notation of the electronic state
  97-100  i4    ---   v             State vibrational quantum number
 101-105  i5    ---   Lambda        Projection of electonic angular momentum
 106-111  f6.1  ---   Sigma         Projection of the electronic spin
 112-117  f6.1  ---   Omega         Projection of the total angular momentum
 118-121  a4    ---   Ca/EH/Ma/Sh   Calculated (Ca), Effective Hamiltonian (EH)
                                    MARVEL (Ma), Shifted from calculation (Sh)
 122-135  f14.6 cm-1  E_Duo         Calculated energy term value in cm-1
 -------------------------------------------------------------------------------

Byte-by-byte description of the partition function files *.pf
-------------------------------------------------------------------------------
  Bytes Format Units   Label  Explanations
-------------------------------------------------------------------------------
  1- 13 f13.3    K      T     Temperature 
 15- 34 e20.8   ---     Q     Partition function
 ------------------------------------------------------------------------------

Contacts:
   J. Tennyson,  j.tennyson@ucl.ac.uk
   S.N. Yurchenko, s.yurchenko@ucl.ac.uk
===============================================================================