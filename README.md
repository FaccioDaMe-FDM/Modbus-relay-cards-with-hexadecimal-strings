# Modbus-relay-cards-with-hexadecimal-strings

# Home Assistant integration of relay module with Modbus TCP Hex Strings on rs485 serial port.

To make the integration work, you must replace the following values in the code:

- converter IP address
- converter port

<img width="926" height="375" alt="example_code" src="https://github.com/user-attachments/assets/9fc325b3-ec87-4d61-aeb3-d75836b5ffc6" />



# To make the integration work, you need to add the ''TCPSENSOR'' add-on and to add it you need to install HACS:

HACS Install:

- go to Home assistant terminal and lunch this command 

wget -O - https://install.hacs.xyz | bash -

TCPSENSOR Install:

Add this custom repository '' https://github.com/se3/tcpsensor '' as Integration in HACS menu and click download


# 2_channel_module :

<img width="698" height="414" alt="module" src="https://github.com/user-attachments/assets/f8fb2b3d-63b6-407e-ab7d-8ee484a704c0" />

https://it.aliexpress.com/item/1005002805597285.html?invitationCode=Z2lmVnpjZlQrVEwwdXIvYTVIMlBWTDJ2RTJqRU1wcUprS0M0eU5ScTRlYWVQemFTZUJrNWVWT0s1MU1hdTAyWg&srcSns=sns_Copy&spreadType=productdetail&bizType=sellerinvite&social_params=61187723806&spreadCode=Z2lmVnpjZlQrVEwwdXIvYTVIMlBWTDJ2RTJqRU1wcUprS0M0eU5ScTRlYWVQemFTZUJrNWVWT0s1MU1hdTAyWg&aff_fcid=bb66f2be99cd405081569e4055472fcd-1752934819623-03226-_Ey7VB3u&tt=MG&aff_fsk=_Ey7VB3u&aff_platform=default&sk=_Ey7VB3u&aff_trace_key=bb66f2be99cd405081569e4055472fcd-1752934819623-03226-_Ey7VB3u&shareId=61187723806&businessType=ProductDetail&platform=AE&terminal_id=52e5c6863bdc4886aba85dc3bddb4a96&afSmartRedirect=y



# 4_channel_module :

<img width="757" height="570" alt="module" src="https://github.com/user-attachments/assets/00109645-4363-4c16-966f-dac88bb385f8" />

https://it.aliexpress.com/item/4000240777004.html?invitationCode=Z2lmVnpjZlQrVEwrRTl6RVUzY1VpNzJ2RTJqRU1wcUprS0M0eU5ScTRlYWVQemFTZUJrNWVWT0s1MU1hdTAyWg&srcSns=sns_Copy&spreadType=productdetail&bizType=sellerinvite&social_params=61183730058&spreadCode=Z2lmVnpjZlQrVEwrRTl6RVUzY1VpNzJ2RTJqRU1wcUprS0M0eU5ScTRlYWVQemFTZUJrNWVWT0s1MU1hdTAyWg&aff_fcid=232060bdb27b418d984dca2ba66a7552-1752935053453-09270-_EIghf9y&tt=MG&aff_fsk=_EIghf9y&aff_platform=default&sk=_EIghf9y&aff_trace_key=232060bdb27b418d984dca2ba66a7552-1752935053453-09270-_EIghf9y&shareId=61183730058&businessType=ProductDetail&platform=AE&terminal_id=52e5c6863bdc4886aba85dc3bddb4a96&afSmartRedirect=y



# 8_channel_module :

<img width="844" height="456" alt="module" src="https://github.com/user-attachments/assets/5b832c98-c1e7-4572-8186-6066c895e3ae" />


https://it.aliexpress.com/item/4000146850177.html?invitationCode=Z2lmVnpjZlQrVElSQ05RSzE5ek4rYjJ2RTJqRU1wcUprS0M0eU5ScTRlYWVQemFTZUJrNWVWT0s1MU1hdTAyWg&srcSns=sns_Copy&spreadType=productdetail&bizType=sellerinvite&social_params=61177186520&spreadCode=Z2lmVnpjZlQrVElSQ05RSzE5ek4rYjJ2RTJqRU1wcUprS0M0eU5ScTRlYWVQemFTZUJrNWVWT0s1MU1hdTAyWg&aff_fcid=e734b4ef6a1f4061924fbf6c5d31c43c-1752935061612-04077-_EJ4m17u&tt=MG&aff_fsk=_EJ4m17u&aff_platform=default&sk=_EJ4m17u&aff_trace_key=e734b4ef6a1f4061924fbf6c5d31c43c-1752935061612-04077-_EJ4m17u&shareId=61177186520&businessType=ProductDetail&platform=AE&terminal_id=52e5c6863bdc4886aba85dc3bddb4a96&afSmartRedirect=y



# rs485 to eth or wifi converter

I recommend using this one, but you can use any similar device:

<img width="572" height="562" alt="elfin" src="https://github.com/user-attachments/assets/35433276-e888-4208-9d5b-95cf4148f38c" />

https://a.aliexpress.com/_EzQiFGI


# settings :

<img width="952" height="870" alt="serial_settings" src="https://github.com/user-attachments/assets/8fe41bf5-26fa-4fd9-829c-69c1e861a6d4" />


<img width="954" height="846" alt="communication_settings" src="https://github.com/user-attachments/assets/21ed36a2-efd2-459c-b7a3-16cd7817af1c" />


# Warning : 

It may happen that the switch you created, which will control the various relays, does not execute its function when pressed, as the command line command is occasionally not sent.
As long as it's a manual activation, there's no problem; simply press it again. However, if an automation is doing it, it becomes a problem. Therefore, it's sufficient to insert a routine into the automation that sends the command three times when the command is activated.
Furthermore, by inserting a four-second delay before the action, the problem occurs much less frequently.



