# liberate-formula
Formula for SUSE Manager / Uyuni to convert systems from EL clones to SUSE Liberty Linux

*This repo is now deprecated, please use*:
https://github.com/SUSE/salt-formulas/tree/master/liberate-formula

Keeping the rest of the content for achiving purposes ...

Please check [Quickstart](Liberate-Quickstart.md) to learn how to use it

This is the result of the Hackweek 23 project:
https://hackweek.opensuse.org/23/projects/use-uyuni-to-migrate-el-linux-to-sll

# Release a version in OBS
OBS project: https://build.opensuse.org/package/show/home:RDiasMateus:uyuni/liberate-formula

## Version testing status 


| OS version  | Status 0.1 | Status Main |
| ----------- | ---------- | ----------- |
| Rhel 9      | Working | Not Tested |
| Rocky 9     | Working | Not Tested |
| Alma 9      | Working | Not Tested |
| Oracle 9    | Working | Not Tested |
| Rhel 8      | Working | Not Tested |
| Rocky 8     | Working | Not Tested |
| Alma 8      | Working | Not Tested |
| Oracle 8    | Working | Not Tested |
| Rhel 7      | Not Tested | Not Tested |
| CentOS 7    | Working | Not Tested |
| Oracle 7    | Working | Not Tested |

# Notes

Analyze if the workaround for EL flavors different from RHEL and CentOS can be removed. Check project https://build.suse.de/package/view_file/SUSE:SLL-9:Import/sll-release/sll-release.spec?expand=1

Salt State & Formula tasks done:
- remove `/usr/share/redhat-release`: DONE
- remove `/etc/dnf/protected.d/redhat-release.conf`: DONE
- install SLL package: DONE
- re-install all packages from SLL channels: DONE 
- add option in Formula and UI to select reinstall: DONE

RPM Build tasks done:
- adapt the version number in the spec file
- add changes entry
- create a local tag and upload it to the repo
- Create a release in git
- download the tar file and save it to the OBS project
- Copy the spec and changes file to the OBS project
- add and commit all to OBS project
