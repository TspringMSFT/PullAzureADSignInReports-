# PullAzureADSignInReports-
Azure AD Sign In Reports are critical to understanding user authentication to AAD and security related concerns. This capability was initially announced on the Enterprise Mobility Blog.   The Sign In reporting is awesome since it is a one stop shopping experience for the sign in auditing for all sign in activity to your Azure AD tenant. In other words, if a user signs into Exchange services (Office 365 Exchange Online)  there is a sign in entry related to that. If they sign in to Office application the it will appear as Office 365. This list goes on for each Microsoft online service accessible by your users.

This script uses Active Directory Authentication Language (ADAL) libraries for authentication. ADAL must be installed via Azure PowerShell or the Azure SDK for authentication to work. 

Simply enter your tenant ID and replace the made up one in the script.  Your tenant ID is available in your Azure AD portal blad for Properties. It is the directory ID field. You can also alter the $URL variable to change the date range or other filtering options for the script to query.  Here is the link to this page: https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties .

The script queries the Azure AD Audit Graph endpoint for Sign In report entries.  More information about the filtering options and the data returned can be found online at this link: https://docs.microsoft.com/en-us/graph/api/resources/signin?view=graph-rest-beta .

This script is an as-is resource.  Please use it but adapt it for your organizations needs. However, be aware that the data format that is returned is static in this code but the Graph data returned can change without warning.  You may need to update the script at some point if the sign in data schema changes!  

If you need a dynamic scripted method you can download the Microsoft provided script from the Sign Ins blade here https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/SignIns .  That script dynamically assigns data to columns and is resilient on data schema changes.
