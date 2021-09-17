# Windows command line goodies
- Show and modify (file extension, filetype) associations: 
  ```
  assoc
  ```
- Show and modify (filetype, command) associations:
  ```
  ftype
  ```
- Show group policies applied to a user and domain group membership
  ```
  gpresult /V
  ```
- Show group membership of any domain user
  ```
  net user USERNAME /domain
  ```
- Obtain information about processors, CPU, cores, etc.
  ```
  wmic cpu
  ```
- How to know the details of a user behind a domain username (including password expiration date)
  ```
  net user <USERNAME> /DOMAIN
  ```
# Common questions

- [How are Word documents locked? (and how to unlock them)](https://support.microsoft.com/en-us/help/313472/the-document-is-locked-for-editing-by-another-user-error-message-when)
- Windows network proxy configuration
  - [Windows proxy settings explained](https://web.archive.org/web/20200529125414/https://securelink.net/en-be/insights/windows-proxy-settings-explained/), explanation of the 3 major ways to use proxy servers in Windows: per-app settings, WinINET (the one used by Internet browsers) and WinHTTP
  - [How to use Fiddler as a WinHTTP proxy](https://www.telerik.com/blogs/using-fiddler-with-winhttp)
