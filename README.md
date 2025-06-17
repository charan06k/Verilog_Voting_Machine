# Verilog Voting Machine
This project is about making a minimilist voiting machine using a HDL (hardware Discpriptive Language) verilog and implement it on Nexys 4 DDR FPGA   

The main motive of the voting machine as follows:  

The core FSM manages the voting process across four states:–  
**1. IDLE**: Awaits the admin code (sw == admin_code) and btn_ov_cv to enter VOTING_OPEN.    

**2. VOTING_OPEN**: Enables voting via btn_1, btn_2, or btn_3; LEDs flash(enable_leds = 1). Exits to VOTING_CLOSED with admin code and btn_ov_cv.   

**3. VOTING_CLOSED**: Waits three 1 Hz cycles (vc_ctr counts to 2’b11) before moving to DISPLAY_WIN.   

**4. DISPLAY_WIN**: Shows the winner; returns to IDLE on btn_ov_cv.   

