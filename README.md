# Files External Google Drive (Nextcloud app)
  ## THIS IS A FORK
  I probabably reinvented the wheel as I did not see there were multiple branches. I added some customizations and it kinda works. Seems to work somewhat slowly to upload files (maybe just was my bad server specs)
  Google Drive external storage support for Nextcloud (still in Beta)

# installation
## From the appstore
- Simply install `files_external_gdrive` from the Nextcloud appstore

## From git
- First, clone the repo `git clone https://github.com/NastuzziSamy/files_external_gdrive.git`
- Execute `make install` in the app directory
- And enable the app with `php occ app:enable files_external_gdrive` in the Nextcloud directory

# TODOs
- [x] Make files and directories:
    - [x] Printable
    - [x] Readable
    - [x] Downloadable
    - [x] Uploadable
    - [x] Editable
    - [x] Renamable
    - [x] With the right mimetype
- [ ] Allow regular user to create its own Google Drive external storage
- [ ] Print better stats
- [ ] Update only on changes
- [ ] Optimize
- [ ] Fix Oauth duplications
- [ ] Unit tests

# Changelogs
### v0.2.8
- Bug fixed:
    - Rename create an error https://github.com/NastuzziSamy/files_external_gdrive/issues/8

### v0.2.7
- Bug fixed:
    - In certain php version, some functions returned errors

### v0.2.6
- Bugs fixed:
    - Correct Oauth2 grant bug https://github.com/NastuzziSamy/files_external_gdrive/issues/4
    - Storage was all time "temporarily not available" https://github.com/NastuzziSamy/files_external_gdrive/issues/5
    - Building path did not work correctly with root

### v0.2.5
- Bug fixed:
    - Add vendor directory in the nextcloud app https://github.com/NastuzziSamy/files_external_gdrive/issues/1

### v0.2.4
- Add installation procedure
- Improve the appinfo.xml file

### v0.2.3
- Bugs fixed:
    - It was impossible to install the app from the appstore (Makefile missing..) https://github.com/NastuzziSamy/files_external_gdrive/issues/1

### v0.2.2
- Bugs fixed:
    - Files were all time exported (and sometimes, in an incompatible format) https://github.com/NastuzziSamy/files_external_gdrive/issues/3
    - Files were not downloaded correctly (files streams were badly requested)

### v0.2.1
- Make the app compliant
- Be warn the app is still in beta version until v1.0.0

### v0.2.0
- Add test function
- Force Nextcloud to update all directories contents
- Final Google compatibility
- Google files are automaticaly exported in the good file type
- Files and directories are now deletable
- First publication on Nextcloud appstore

### v0.1.0
- Based on the work of the Google Drive external storage support for ownCloud
- Use of Flysystem fonctionnality
- Switch Google API v2 to v3
- Google files and directories are
    - Printed
    - Readable
    - Downloadable
    - Editable
    - Renamable
