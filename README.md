# EtherCAT-ESI-File-Examples
An example of how to manually edit an EtherCAT ESI File to edit the PDO mapping.
Typically, an EtherCAT master will map the user-mappable PDO's on system startup using an SDO initialization sequence.
However, some masters do not provide the SDO initialization capability to the user and require the user to manually edit the ESI file to edit the PDO mapping.
Entries can be added to TxPDO's (0x1a00-0x1a03) and RxPDO's (0x1600-0x1603) directly in the file.
Each of these 8 user-mappable PDO's can contain up to 32 bytes of data.
See line 16515 of "Copley_XE2_4.60.xml" for an example of how to add an entry to a user-mappable PDO.
In the example, the general purpose inputs (0x219a) are added to TxPDO1 (0x1a00).
