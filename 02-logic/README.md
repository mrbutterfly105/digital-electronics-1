# Lab 2: Tomáš Paulysko

### 2-bit comparator

1. Karnaugh maps for other two functions of 2-bit comparator:

   Greater than:

  ![IMG_0823](https://user-images.githubusercontent.com/102173814/220767881-b7486fa6-51f8-4c13-84f2-223eabfdab71.jpg)


   Less than:

   ![IMG_0822](https://user-images.githubusercontent.com/102173814/220767938-21a80762-1fe0-4e59-9e65-6537dd68dfb8.jpg)


2. Mark the largest possible implicants in the K-map and according to them, write the equations of simplified SoP (Sum of the Products) form of the "greater than" function and simplified PoS (Product of the Sums) form of the "less than" function.

   ![IMG_0821](https://user-images.githubusercontent.com/102173814/220768350-3b9fbd11-e036-453a-aff5-7764b056a9c4.jpg)

   ![IMG_0820](https://user-images.githubusercontent.com/102173814/220767983-3a340d46-3810-40c6-8585-3e6f6adaf4cf.jpg)

### 4-bit comparator

1. Listing of VHDL stimulus process from testbench file (`testbench.vhd`) with at least one assert (use BCD codes of your student ID digits as input combinations). Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

   Last two digits of my student ID: **xxxx31**

```vhdl
    p_stimulus : process
    begin
        -- Report a note at the beginning of stimulus process
        report "Stimulus process started" severity note;

        -- First test case
        s_b <= "0011"; 
        s_a <= "0001"; 
        wait for 100 ns;
        -- Expected output
        assert ((s_B_greater_A = '1') and
                (s_B_equals_A  = '0') and
                (s_B_less_A    = '0'))
        -- If false, then report an error
        report "Input combination 0011, 0001 FAILED" severity error;

        -- Report a note at the end of stimulus process
        report "Stimulus process finished" severity note;
        wait;
    end process p_stimulus;
```

2. Link to your public EDA Playground example:

  https://www.edaplayground.com/x/kYkx
