# gistnc - A gist synchronization tool

![](https://img.shields.io/github/languages/top/badges/shields.svg) ![](https://img.shields.io/github/license/festum/gistnc-bin.svg) ![](https://img.shields.io/github/downloads/festum/gistnc-bin/latest/total.svg) ![](https://img.shields.io/github/tag/festum/gistnc-bin.svg)

## Features

- Sync
- AES256 encryption

## Getting start

- Download the binary from [release page](https://github.com/festum/gistnc-bin/releases)
- Made a configuration file `.gistnc.yml` in binary directory
- Run command ./gistnc sync

## Configuration

```.gistnc.yml
token: YOUR_GIST_TOKEN
gists:
  YOUR_GIST_ID_1:
    folder_path: YOUR_LOCAL_PATH_1
	  - YOUR_FILE_1
  YOUR_GIST_ID_2:
    folder_path: YOUR_LOCAL_PATH_2
    enabled_files:
      - YOUR_FILE_1
	  - YOUR_FILE_2
remote_encryption: true
```

Don't you know the token yet? See [here](https://developer.github.com/apps/building-oauth-apps/creating-an-oauth-app/) to get one.
For getting your Gist ID you can go `https://api.github.com/users/:username/gists` to find it.
Even private Gist is able to read by everyone only id you know the Gist ID. Thus, set `remote_encryption` as true is recommended.
