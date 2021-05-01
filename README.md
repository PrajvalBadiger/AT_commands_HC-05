# AT commands for HC-05

This project demonstrates configuring HC-05 bluetooth module with AT commands. <br>

## Requirements

1. Arduino Nano
2. HC-05 bluetooth module
3. Jumper wires
3. Arduino IDE

## Connection

1. HC-05 Rx -> D6 on Arduino
2. HC-05 Rx -> D5 on Arduino
3. HC-05 Vcc -> Vcc on Arduino
4. HC-05 Gnd -> Gnd on Arduino

Connect power while holding the reset button on the HC-05 module,
this puts the module into AT command mode.

## Commands

1. Upload the given [`sketch`](/arduino_as_serial.ino) to Arduino Nano
2. Open the Serial Monitor, set the Baud rate to 9600 and Both Nl & CR
3. Enter the following commands

<table>
	<tr>
		<th> commands </th>
		<th> Response </th>
		<th> Function </th>
	</tr>
	<tr>
		<td> AT </td>
		<td> OK </td>
		<td> Test connection </td>
	</tr>
	<tr>
		<td> AT+NAME? </td>
		<td> Name of the device </td>
		<td> Display name of the device </td>
	</tr>
	<tr>
		<td> AT+NAME=MY-BT </td>
		<td> OK </td>
		<td> Set device name to MY-BT </td>
	</tr>
	<tr>
		<td> AT+PSWD? </td>
		<td> passkey </td>
		<td> Display pairing pin </td>
	</tr>
	<tr>
		<td> AT+PSWD=1234 </td>
		<td> OK </td>
		<td> Set pairing pin to 1234 </td>
	</tr>
	<tr>
		<td> AT+UART?</td>
		<td> +UART=param1,param2,param3 <br> OK </td>
		<td> print baud rate (param1), stop bit (param2) and parity (param3)</td>
	</tr>
	<tr>
		<td> AT+UART=param1,param2,param3 </td>
		<td> OK </td>
		<td> Set baud rate to param1, stop bit to param2 and parity to param3 <br>
			Ex: AT+UART=57600, 1,2</td>
	</tr>
<table>

For more AT commands refer this 
<a href="https://www.itead.cc/wiki/Serial_Port_Bluetooth_Module_(Master/Slave)_:_HC-05"> link </a>.
