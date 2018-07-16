To install this correctly into the romfs folder:

1. Move pam_script.so to /lib (NOT /lib/security)
2. Rename README-for-pamscript to README
3. Move pam_script and README to /etc/default
4. Create a folder called pam-script.d/
5. Create symbolic links to pam_script called: 
  -pam_script_acct 
  -pam_script_auth
  -pam_script_passwd
  -pam_script_ses_close
  -pam_script_ses_open
