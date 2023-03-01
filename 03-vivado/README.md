# Lab 3: Tomáš Paulysko

### Three-bit wide 4-to-1 multiplexer

1. Listing of VHDL architecture from source file `mux_3bit_4to1.vhd`. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture Behavioral of mux_3bit_4to1 is
begin
with sel select
      y_o <= a_i when "00",  -- If addr_i = "000" then y_o = a_i
           b_i when "01",
           c_i when "10",
           d_i when others; -- All other combinations


end architecture Behavioral;
```

2. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

<img width="1390" alt="Snímek obrazovky 2023-03-01 v 22 28 02" src="https://user-images.githubusercontent.com/102173814/222268856-d2289170-810e-43ef-9a91-5e04edb25412.png">


3. Listing of pin assignments for the Nexys A7 board in `nexys-a7-50t.xdc`. **DO NOT list** the whole file, just your switch and LED settings.

```shell
# I WAS USING EDA, SO THIS TASK IS IRELEVANT
```
