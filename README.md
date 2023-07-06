
## Changelog
forked from https://github.com/rehroman/dropbox-file-downloader and modified to support download of nested folders.


# Dropbox File Downloader

This is a Python script that uses the Dropbox API to download files from a shared Dropbox folder.

## Requirements

- Python 3.6 or above
- `requests` library

You can install the `requests` library using pip:

```
pip install requests
```
## Usage
The script can be run from the command line with the following syntax:

```
python dropbox_download.py -t YOUR_ACCESS_TOKEN -url YOUR_SHARED_FOLDER_LINK
```
Replace YOUR_ACCESS_TOKEN with your Dropbox API access token.
To receive your token, go for example to https://dropbox.github.io/dropbox-api-v2-explorer/#files_list_folder, press 'Get Token' and completely copy it.

Replace YOUR_SHARED_FOLDER_LINK with the URL of the Dropbox folder you wish to download from. Take the full shared link you received and don't copy the URL from your browser after opening it. There is a "rlkey=" part in the correct one. You can also go into a subfolder, but keep in mind to add the part beginning with "&rlkey" from the original URL in the end.

## Options
The script also supports the following optional arguments:
```
-t, --token: your token. To get the api token https://dropbox.github.io/dropbox-api-v2-explorer/#files_list_folder
-url : Shared Dropbox folder link.
-df, --download_folder: Sets the destination download folder (default is "dropbox_download").
-f, --folder: Remote folder to download, useful for recursive calls to nested folders. e.g., if folder name is "Name" insert "/Name". If empty start downloading from the root of the shared dropbox folder.
-c, --count: Sets the number of files to download (default is all files).
-v, --verbose: Prints the full API response.
-h: Displays these information.
```

## Dropbox API information

- https://www.dropbox.com/developers/documentation/http/documentation

