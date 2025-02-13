## R CMD check results

0 errors ✔ | 0 warnings ✔ | 0 notes ✔

* This is a new release.


### Mail from Prof Brian Ripley: 
On macOS this often, including today, when checking brings up a modal
dialog box saying the your package

'wants to access confidential information in your keychain'

and asking for my password.  This was a clear violation of the CRAN
policy, so the package has been removed from CRAN.

Response: The modal dialog appears due to the use of the Keyring package, which is employed to store the necessary credentials for using the package. I understand that this behavior is not compliant with CRAN policies.
To address this, I removed the dependency on Keyring and switch to using environment variables instead, ensuring that this issue does not occur in future versions.



### Benjamin Altmann: For your next update:
Please add a web reference for the API in the form <https:.....> to the
description of the DESCRIPTION file with no space after 'https:' and
angle brackets for auto-linking.
For more details:
<https://contributor.r-project.org/cran-cookbook/description_issues.html#references>
