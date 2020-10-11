# win10-enable-enforcement-mode
Registry values for enforcement mode Windows 10

# Instalation
Download *EnableEnforcementMode.reg* file into your computer.

Run (double click.

No reboot required.

Enjoy!



Due to a critical security problem, Microsoft announced the two-phase vulnerability approach, with the first phase being an update on August 11, 2020, and the second phase being an update to be released in the first quarter of 2021. Until the next update, an additional device security measure is launching the "enforcement" mode of the Domain Controller. 


# Below is the text from official site (Microsoft):
https://support.microsoft.com/en-us/help/4557222/how-to-manage-the-changes-in-netlogon-secure-channel-connections-assoc#EnforcementMode

***Warning 
Serious problems might occur if you modify the registry incorrectly by using Registry Editor or by using another method. These problems might require that you reinstall the operating system. Microsoft cannot guarantee that these problems can be solved. Modify the registry at your own risk.

The August 11, 2020 updates introduce the following registry setting to enable enforcement mode early. This will be enabled regardless of the registry setting in the Enforcement Phase starting on February 9, 2021: 

Registry subkey	
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Netlogon\Parameters

Value	
FullSecureChannelProtection

Data 
type	REG_DWORD

Data
1 – This enables enforcement mode. DCs will deny vulnerable Netlogon secure channel connections unless the account is allowed by the Create Vulnerable Connection list in the "Domain controller: Allow vulnerable Netlogon secure channel connections" group policy.  

0 – DCs will allow vulnerable Netlogon secure channel connections from non-Windows devices. This option will be deprecated in the enforcement phase release.


Reboot required?	No
