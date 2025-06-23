## R CMD check results

0 errors ✔ | 0 warnings ✔ | 0 notes ✔

* This is a new release.

###  Mail from Uwe Ligges

"For us, all three of

https://is.gd/SQyA8D
https://www.bigdata.pe.gov.br
https://www.wiki.pe.gov.br/mediawiki/index.php/Plataforma_de_Compartilhamento_e_An%C3%A1lise_de_Dados

timed out again."

Response: I just found out that most government domains under pe.gov.br are not accessible from outside Brazil. Apparently, this is a "security policy" set by the state’s IT agency...
I’m working on getting some of these addresses whitelisted, but in the meantime, I’ll remove the link to avoid any issues. Thanks for your patience!


###  Mail from Uwe Ligges
"Found the following (possibly) invalid URLs:
     URL: https://is.gd/SQyA8D
       From: DESCRIPTION
       Status: Error
       Message: Connection timed out after 60002 milliseconds

(also from my local machine with Firefox).
Any ideas?
"

Response: The URL in the DESCRIPTION was supposed to be https://www.bigdata.pe.gov.br, 
but it is currently pointing to a wikipage link. It turns out both addresses require
internal access to the pe.gov.br network or a VPN, so external connections time out. 
I’m looking for a publicly accessible reference for BigDataPE to replace this private 
link. Sorry for the inconvenience, and I’ll update the link once we have a 
publicly accessible resource.

I’m now trying to use a shorter, publicly accessible link for BigDataPE:
https://www.wiki.pe.gov.br/mediawiki/index.php/Plataforma_de_Compartilhamento_e_An%C3%A1lise_de_Dados

Hopefully, this link won’t time out or require internal network access. Let me know if you still encounter any issues.

### Mail from Prof Brian Ripley: 
"On macOS this often, including today, when checking brings up a modal
dialog box saying the your package

'wants to access confidential information in your keychain'

and asking for my password.  This was a clear violation of the CRAN
policy, so the package has been removed from CRAN.""

Response: The modal dialog appears due to the use of the Keyring package, which is employed to store the necessary credentials for using the package. I understand that this behavior is not compliant with CRAN policies.
To address this, I removed the dependency on Keyring and switch to using environment variables instead, ensuring that this issue does not occur in future versions.



### Benjamin Altmann: For your next update:
Please add a web reference for the API in the form <https:.....> to the
description of the DESCRIPTION file with no space after 'https:' and
angle brackets for auto-linking.
For more details:
<https://contributor.r-project.org/cran-cookbook/description_issues.html#references>
