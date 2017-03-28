# Template-TypeScript-GoogleAppsScript

## How to Initialize

If you have initialized `node-google-apps-script` already, skip to 3.

1. Install `node-google-apps-script`

    ```bash
    $ yarn global add node-google-apps-script
    ```

2. Configure authorized information. 

    1. Go GoogleAPI Console and create new project or select an exist project.
    2. Activate DriveAPI to access Drive file. 
    3. Create OAuth information and download authorized json file.
    4. Register authorized json file.

        ```bash
        $ gapps auth <authorized_json_file>
        ```

3. Configure Google Apps Script Project.

    1. Create Googl Apps Script Project or select an exist project.
    2. Get FileID. FileID is included in the url such as `https://script.google.com/d/<FileID>`.
    3. Register FileID.

        ```bash
        $ gapps init <FileID>
        ```
That's all. You can upload files under `/src` by running `gapps upload` command.