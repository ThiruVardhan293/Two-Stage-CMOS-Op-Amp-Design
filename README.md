Two-Stage CMOS Op-Amp Design Report 
Technology: 180nm TSMC 
Tool: LTspice 
1. Design Specs 
● DC Gain ≥ 60 dB 
● Phase Margin ≥ 60° 
● Slew Rate ≥ 20 V/µs 
● ICMR: 0.8 V to 1.6 V 
● Load Capacitance: 2 pF 
● GBW = 30 MHz 
● Power ≤ 300 µW 
● VDD = 1.8 V 
2. Design Summary 
We designed a two-stage op-amp with Miller compensation and simulated it in LTspice. 
Initially, the gain was 52 dB and phase margin around 62°. We increased the gain to 64 dB by 
widening the NMOS transistor in the second stage, which increased output resistance and thus 
the gain, without significantly affecting phase margin. 
3. Key Design Calculations 
● Compensation capacitor (Cc): 
Cc ≥ 2.2 × CL = 440 fF → We used 800 fF 
● Slew Rate (SR = I5 / Cc): 
I5 = 800 fF × 20 V/µs = 16 µA → taken as 20 µA 
● GBW = gm1 / Cc → gm1 = 
30 MHz × 800 fF = 24 µS 
● W/L for M1, M2: 
Based on gm1 = 24 µS and Id = 7 µA 
→ W/L ≈ 9 (adjusted for better gain and vdsat5) 
● W/L for M3, M4 (using ICMR+ condition): 
Calculated ≈ 14 
● W/L for M5 (using ICMR− condition): 
Adjusted to get Vdsat 5 > 100 mV → W/L = 20 
● Second Stage: gm6 ≥ 10 × gm1 → gm6 = 240 µS 
Based on this, W/L6 ≈ 174, and bias current I6 ≈ 125 µA 
● W/L7 (current mirror): 
Based on I6/I5 = 125/20, W/L7 = 125 
4. Simulation Results 
● DC Gain: 64 dB 
● Phase Margin: ~62° 
● GBW: 36 MHz 
● Slew Rate: ≥ 20 V/µs 
● ICMR Supported: 0.8 V – 1.6 V 
● Power Consumption: < 300 µW 
