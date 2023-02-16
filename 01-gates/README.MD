# Lab 1: Tomáš Paulysko

### De Morgan's laws

1. Equations of all three versions of logic function f(c,b,a):

   <img width="401" alt="Snímek obrazovky 2023-02-16 v 0 07 20" src="https://user-images.githubusercontent.com/102173814/219210740-b8fd8681-7c07-464b-981b-1c3b34917aa9.png">


2. Listing of VHDL architecture from design file (`design.vhd`) for all three functions. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture dataflow of gates is
begin
    f_orig_o <= (not(b_i) and a_i) or
                (c_i and not(b_i or not(a_i)));
    f_nand_o <= (not(b_i) and a_i and not(c_i)) and (not(b_i) and not(a_i) and not(c_i)) and (b_i and not(a_i));
    f_nor_o  <= (not b_i or a_i or not c_i) or (not b_i or not a_i or not c_i) or (b_i or not a_i);
end architecture dataflow;
```

3. Complete table with logic functions' values:

   | **c** | **b** |**a** | **f_ORIG** | **f_(N)AND** | **f_(N)OR** |
   | :-: | :-: | :-: | :-: | :-: | :-: |
   | 0 | 0 | 0 | 0 | 0 | 0 |
   | 0 | 0 | 1 | 1 | 1 | 1 |
   | 0 | 1 | 0 | 0 | 0 | 0 |
   | 0 | 1 | 1 | 0 | 0 | 0 |
   | 1 | 0 | 0 | 0 | 0 | 0 |
   | 1 | 0 | 1 | 1 | 1 | 1 |
   | 1 | 1 | 0 | 0 | 0 | 0 |
   | 1 | 1 | 1 | 0 | 0 | 0 |

### Distributive laws

1. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   <img width="1376" alt="Snímek obrazovky 2023-02-15 v 23 44 52" src="https://user-images.githubusercontent.com/102173814/219206943-9a6e7fa1-56f2-4731-8bb2-d7c154680856.png">


2. Link to your public EDA Playground example:

   [https://www.edaplayground.com/...](https://www.edaplayground.com/x/5L92)
