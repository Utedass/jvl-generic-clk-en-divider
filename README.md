# jvl-generic-clk-en-divider

Jegatron VHDL Library - Generic Clock Enable Divider

Entity: generic_clk_en_divider

Declarating

```vhdl
	component generic_clk_en_divider is
		generic (
			divider_bits : integer := 8
		);
		port
		(
			clk : in std_logic;
			rstn : in std_logic;
			en  : in std_logic;
			en_out : out unsigned (divider_bits - 1 downto 0)
		);
	end component;
```

Instansiating

```vhdl
	my_9_bit_divider : generic_clk_en_divider
		generic map(
			divider_bits => 9
		)
		port map(
			clk => my_clock_signal,
			rstn => my_resetn_signal,
			en => my_enable_signal,
			en_out => my_divided_en_signals
		);
```
