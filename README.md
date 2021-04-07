# Dynamic-Email-System

Send Templatized Dynamic Emails Automatically

## Features

This is a simple program which does its work perfectly. Nothing more, nothing less

1. Send dynamic emails with unlimited variables pulling data from a CSV file.
2. Supports Markdown Formatting & embed links or images.
3. Supports Attaching any kind of files.

## Usage

- Make sure you have Python installed in your system.
- Download or Clone the repo and then move into the `automailer` directory.
- Install all dependancies:
  ```shell
  pip install -r requirements.txt
  ```
- Write your email inside **`compose.md`** (supports markdown formatting)
- You can use **variables** , prefix them with `$` sign.

  > Hi $NAME , your IP address for $DOMAIN is $IP_ADDRESS

- Put your data inside `data.csv` file
  _The line 1 ie headers must contain 'EMAIL' (uppercase) parameter_

  ![CSV_file](https://user-images.githubusercontent.com/71599504/113860951-46ac1900-97c4-11eb-9155-735d22cf537e.jpg)

  _You can Export CSV file from Microsoft Office Excel, Libre Office, Google Sheets, SQL Database, or NoSQL Database_

- If you want to put any attachments , put them in the `ATTACH` directory.
- Create a file `.env` for environment variables and put the following into it:

  ```text
  display_name=Mr.Harvey
  sender_email=your@example.com
  password=12345
  ```

  _Make sure to put real values, the above values are just an example_

- **Do not put original email password.**
  Create Gmail Account then turn on 2 step Verification, and then set up an [App Password](https://support.google.com/accounts/answer/185833?hl=en) for `automailer`.
- All set up 👍 you are now READY TO GO . Run the `send.py` file:
  ```shell
  python3 send.py
  ```
- You will be asked to confirm the attachments in the `ATTACH` folder. Upon confirmation , the application will start sending emails.
- You will receive a full success report after emails are sent.

## Getting Help

Please report an issue or ask your question in the issues section of the repository.
