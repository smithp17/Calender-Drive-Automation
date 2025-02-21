# 📅 Calendar-Drive Automation

This project automates the creation of Google Drive folders and generation of PDFs when a new event is created in Google Calendar. The automation also shares the generated folder with the event participants and sends them notification emails.

---

## 🚀 Features

- Automatically creates a Google Drive folder when a Google Calendar event is created.
- Extracts participant emails from the calendar event.
- Saves the latest Google Form response as a PDF in the created folder.
- Sends notification emails to participants with relevant information.
- Logs errors in a specified Google Sheet for tracking.

---

## 📦 Project Structure


---

## 🛠️ Prerequisites

- **Google Account:** Access to Google Calendar, Google Drive, and Google Apps Script.
- **Permissions:** Enable the following services in Apps Script:
  - Calendar API
  - Drive API
  - Gmail API
  - Drive Activity API
- **Google Form:** Form ID should be available and shared in the script.
- **Google Sheet:** Used for error logging.

---

## 📝 Setup Instructions

### 1. **Create a New Google Apps Script Project**

1. Go to [Google Apps Script](https://script.google.com/).
2. Click on **New Project** and rename it (e.g., `Calendar-Drive Automation`).
3. Replace the contents of the default `Code.gs` file with the code from `calendarTrigger.gs`.

---

### 2. **Set Project Properties**

1. In the Apps Script editor, click **Project Settings**.
2. Replace the existing `appsscript.json` content with the provided one.
3. Save the changes.

---

### 3. **Enable Advanced Services and APIs**

1. Go to **Services** in the left panel.
2. Add and enable the following:
   - Calendar API (v3)
   - Drive API (v3)
   - Gmail API (v1)
   - Drive Activity API (v2)
3. Navigate to **Google Cloud Console** and enable the same APIs there.

---

### 4. **Add IDs to the Script**

- Replace placeholders in `calendarTrigger.gs` with your IDs:
  - `CALENDAR_ID`: Use `'primary'` or specific Calendar ID.
  - `FORM_ID`: Insert your Google Form ID.
  - `LOG_SHEET_ID`: Insert your Google Sheet ID.

---

### 5. **Deploy and Authorize the Script**

1. Click **Deploy** > **Test deployments** > **Select type: Web app**.
2. Under "Execute as," select **Me**.
3. Under "Who has access," select **Anyone** or your organization.
4. Click **Deploy** and authorize permissions.

---

### 6. **Create Calendar Trigger**

1. Run the `createTrigger` function in the Apps Script editor.
2. This will set up a trigger to listen for new or updated calendar events.
3. Check **Triggers** in the editor to confirm setup.

---

### 7. **Testing the Automation**

1. Create a new event in your Google Calendar with at least one attendee.
2. Submit a response to the linked Google Form.
3. Check Google Drive:
   - A new folder should be created with a name like `[participantA + participantB Handoff]`.
   - The latest form response should be saved as a PDF in this folder.
4. Check participant emails for notifications.

---

## 📊 Folder & File Structure

Example created folder name:
