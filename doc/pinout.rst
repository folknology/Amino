=====================
Amino Standard Pinout
=====================

The Amino interface definition provides 2 connectors as described below

Female headers that support the blades, view from the top

Extended header available on full slots

=== === 
1V  5V
D9  D10
D11 D12
CO  CK
CI  GND
=== ===

Basic header available on all slots

=== === 
D1  D5
D2  D6
D3  D7
D4  D8
3V3 GND
=== ===

D1-D4 Are single bit digital ports configured individually as inputs or outputs

D5-D12 Can be configured as a single 8 bit or a dual 4 bit port configured either as input or outputs. These can also be reconfigured on the fly an or bitbanged.

CI,CO,CK Are digital signals enabling serial configuration of the blade and or reading of configuration/parameters/operation of the blade. They can also be used in conjunction with D1-12 in order to provide high speed synchronised input and output at multibit widths from 1 bit to 8 bit.




