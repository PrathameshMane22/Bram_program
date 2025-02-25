library ieee;
use ieee.std_logic_1164.all;
use ieee.numeric_std.all;  -- ADD THIS LINE


-- Empty entity for testbench
entity tb_bram is
end tb_bram;

architecture Behavioral of tb_bram is

-- Copy-paste the port declaration of the BRAM from the Xilinx generated file.
component bram_test is
  PORT (
    clka : IN STD_LOGIC;
    ena : IN STD_LOGIC;
    wea : IN STD_LOGIC_VECTOR(0 DOWNTO 0);
    addra : IN STD_LOGIC_VECTOR(7 DOWNTO 0);
    dina : IN STD_LOGIC_VECTOR(15 DOWNTO 0);
    douta : OUT STD_LOGIC_VECTOR(15 DOWNTO 0)
  );
end component;

-- Port signals for connecting with the BRAM
signal clka, ena : std_logic := '0';
signal wea : std_logic_vector(0 downto 0) := "0";
signal addra : std_logic_vector(7 downto 0) := (others => '0');
signal dina, douta : std_logic_vector(15 downto 0) := (others => '0');
constant clk_period : time := 10 ns; -- Clock period.

begin

-- Component instantiation using named association.
bram : bram_test port map(
    clka => clka,
    ena => ena,
    wea => wea,
    addra => addra,
    dina => dina,
    douta => douta);

-- Generate the clock for BRAM
clk_generation: process
begin
    wait for clk_period/2;
    clka <= not clka;
end process;

-- Generate inputs to apply to the BRAM
stimulus: process
begin
    wait for clk_period;
    ena <= '1';
    wea <= "0";

    -- Loop through 256 addresses
    for i in 0 to 256 loop
        addra <= std_logic_vector(to_unsigned(i, 8));
        wait for clk_period;
    end loop;

    wait;
end process;

end Behavioral;
