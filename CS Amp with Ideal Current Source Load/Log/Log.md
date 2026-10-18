
10/10/2026
- To test the amplifier, an arbitrary in range value for W and L for both the MOS transistors were chosen. This should be changed later on.
- Initially the signal was distorted and it turned out the gain was too high and as a result the MOS transistor wouldn't remain in saturation. Lowering the input voltage fixed this issue. 
- The low frequency response is poor. There should be a way to resolve this.
![[PoorLowFreq.png|678]]

11/10/2026
- The body terminals were not connected properly and upon fixing this, the frequency response got better i.e., the low frequency response improved.

![[ImprovedFreResponse.png]]

- Initially, the junction capacitance (Csb and Cdb) were 0, that was because the drain and source parameters like area and perimeter were not defined. Upon defining the parameters, the junction capacitances were no longer 0. 
- Cgd for the given bias is 0. It is because MOS transistor is in saturation, the channel at the drain end is pinched off and thus there is no gate - channel - drain capacitance. But, there is still a gate to drain capacitance which is the overlap capacitance. 

12/10/2026
- Designed the circuit properly by choosing proper values for W and L. Initially the gain was 3 db off the calculations. This was attributed to the loading of the signal at the input side due to the relatively low impedance looking into the current mirror. This was fixed by using a different config shown below.
![[FinalCircuit.png]]

- All the results obtained were thus satisfactory and close to hand calculations from biasing to gain to bandwidth.

13/10/2026
- An interesting observation, the low frequency pole corresponding to Cc1 is around 8 Hz, but despite this fL is close to 0 Hz. This is because the impedance seen at the gate of M1 is infinite and no ac current flows. If we compute the pole and zero due to Cc1, they occur at the same frequency and thus cancel each other. If impedance looking into gate of M1 isnt infinite, then a small ac current flows and the pole and zero due to Cc1 occur at different frequencies. 
- If the original configuration was used, then regardless of whether the impedance looking into gate of M1 was infinite or not, an ac current would flow and the pole and zero corresponding to Cc1 occurs at different frequencies.