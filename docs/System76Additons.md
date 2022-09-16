## Summary

This document provides a quick discription of the files added by system76 to better serve the needs of the company. 

> **Note:** Scripts assume you are running them from the install directory and not in the script folder. 
> 

## jenkins

This script automates the download of the latest nightly iso, and if missing, the current released iso and launches all tests against those images. This script takes no options and is controlled by `/etc/openqa/jenkins.json`.  



## pull_requests

WIP: Downloads and executes tests against current PRs that are ready for testing. In order for the script to work you will need a `.git_token`file in OpenQA's install directory (i.e. `/var/lib/openqa/.git_token`)  



#### Todo:

* The script currently lacks the ability to create a symlink to the newest qcow image found in `/var/lib/openqa/factory/hdd` requiring the operator to create and maintain these links. 

* The version of pop (20.04,22.04,etc.) is hardcoded in the script, furture versions should automatically select the version based on a config file or some other means.
