1) Install Tools
   sudo apt update
   sudo apt install iverilog gtkwave
2) Compile the Design and Testbench
   iverilog -o rv32i_sim iiitb_rv32i.v iiitb_rv32i_tb.v
3) Run the Simulation
   vvp rv32i_sim
4) View Waveforms
   gtkwave dump.vcd
