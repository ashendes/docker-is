# Changelog
All notable changes to this project 5.5.x per each release will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)

## [v5.5.0.5] - 2018-08-17
### Added
- CentOS based dockerfile for Identity Server v5.5.0
- CentOS based dockerfile for Identity Server Analytics v5.5.0
- Alpine and OpenJDK based dockerfile for Identity Server v5.5.0
- Alpine and OpenJDK based dockerfile for Identity Server Analytics v5.5.0

### Changed
- Changed the folders to which configuration files with new changes to be copied are mounted. 
Originally this was <br>"wso2-volume" in general and for kubernetes, this was 
"kubernetes-volumes". But with this release, there will not be <br>any platform specific 
folders for mounting configuration files. Instead we are introducing a single folder 
for this purpose by the name, "wso2-config-volume". 

- Changed the folder to which any other non-configuration type artifacts to be copied are mounted.
Originally this was "wso2-volume". But with this release, this is changed to "wso2-artifact-volume".

### Compatibility with Kubernetes-is releases
- If you are to use images built using this release with the latest v5.5.0.4 kubernetes release, please do change
your deployment mount paths appropriately to match above folder changes.

[v5.5.0.5]: https://github.com/wso2/docker-is/compare/v5.5.0.4...v5.5.0.5