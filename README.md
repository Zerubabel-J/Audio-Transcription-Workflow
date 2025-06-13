Audio Transcription Workflow
![image](https://github.com/user-attachments/assets/82e143ef-ada2-4195-af76-5d5800e307ae)

This n8n workflow automates processing audio files from Google Drive, transcribing them with OpenAI's Whisper API, analyzing with ChatGPT, and storing results in Notion while sending email notifications. It addresses large file issues (>25MB) from a prior Pipedream setup, ensuring reliability and cost-efficiency.
Core Features

*   **Trigger:** Monitors Google Drive for new audio files.
*   **Transcription:** Uses OpenAI Whisper API for accurate audio transcription.
*   **Analysis:** ChatGPT summarizes transcripts and extracts action items.
*   **Output:** Sends email with results and creates a Notion page.
*   **Error Handling:** Logs issues to a Notion database and cleans up temporary files.

Workflow Phases

*   **Google Drive Trigger:** Detects new audio files every 5 minutes.
*   **File Size Check:** Validates files, flags those >25MB.
*   **Download File:** Streams audio file to temporary storage.
*   **Transcribe Audio:** Processes file with Whisper API.
*   **Analyze Transcript:** Generates summary and action items via ChatGPT.
*   **Send Email:** Emails results to user.
*   **Create Notion Page:** Stores transcript and analysis in Notion.
*   **Log Errors:** Records issues in a Notion error log.
*   **Cleanup:** Deletes temporary files.
