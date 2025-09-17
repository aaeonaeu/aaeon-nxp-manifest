# Aaeon Nxp Manifest README

This repository provides manifest files for building AAEON Yocto BSPs on NXP i.MX platforms.


## Introduction

The manifest files in this repository are used with the `repo` tool to set up the Yocto build environment for AAEON boards based on NXP i.MX SoCs.  
They specify the required layers, repositories, and revisions to ensure a reproducible build.


## Manifest Branches

- `*-next`: Development branch.
- Other branches correspond to specific yocto releases.
- The branch will be based on the release type Linux with release manifests in each branch tied to the base releases.
  - For example for i.MX Linux Yocto Project releases the branches will be imx-linux-< yocto-project-release >


## Usage

1. **Install the repo tool**  
    ```
    $: mkdir ~/bin
    $: curl http://commondatastorage.googleapis.com/git-repo-downloads/repo  > ~/bin/repo
    $: chmod a+x ~/bin/repo
    $: PATH=${PATH}:~/bin
    ```


2. **Initialize and sync the repo workspace**
    ```
    $: mkdir <release>
    $: cd <release>
    $: repo init -u https://github.com/aaeonaeu/aaeon-nxp-manifest -b <branch name> [ -m <release manifest>]
    $: repo sync
    ```


3. **Follow the Yocto build instructions**  
   Refer to the each branch's detailed README describing exact syntax


