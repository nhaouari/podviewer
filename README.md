# PodViewer 🎙️✨

PodViewer is an interactive, browser-based tool designed to help you create stunning, shareable video clips from your audio podcasts. It generates a dynamic, colorful background that pulses with your audio and displays perfectly synchronized, word-by-word subtitles, all within a square frame ideal for social media platforms like Instagram, TikTok, and YouTube Shorts.

**➡️ [View the Live Demo](https://nhaouari.github.io/podviewer/)**

![PodViewer Screenshot](https://i.imgur.com/CAnhCAj.png)


## Features

-   **Square Video Format (1:1):** Perfectly sized for social media feeds.
-   **Dynamic Animated Background:** A beautiful, generative lava-lamp effect that moves in time with your audio's frequencies.
-   **Word-by-Word Subtitle Highlighting:** Captivates viewers by highlighting words precisely as they are spoken.
-   **Easy File Uploads:** Simple icon-based buttons to upload your MP3 audio and `.vtt` subtitle files.
-   **Fully Editable Text:** Click to edit the main title and the "Podcast by" credit on the fly.
-   **Modern, Minimal UI:** A clean interface that puts the focus on your content.
-   **No Software Required:** Runs entirely in your web browser. No installs, no plugins.

## How to Create Your Podcast Clip

Follow these steps to generate a professional-looking podcast video clip in minutes.

### Step 1: Generate Your Audio & Subtitles

Before using PodViewer, you need an audio file and a matching subtitle file. A great, free tool for this is **Google AI Studio**.

1.  **Generate Audio:** Go to the [Google AI Studio - Speech Generator](https://aistudio.google.com/generate-speech).
    * Type or paste your script.
    * Choose a voice you like.
    * Click **Generate** and then download the `.mp3` audio file.
2.  **Generate Subtitles:**
    * Use Google AI Studio upload the audio and generate subtitles using vtt.
    * Copy this timestamped text and format it into a `.vtt` file. The structure should look like this:

    ```vtt
    WEBVTT

    00:00.354 --> 00:02.184
    Good evening, everyone.

    00:02.834 --> 00:04.514
    Please hold your applause.

    00:04.884 --> 00:10.164
    My ego is a finely tuned instrument and you're threatening to over-calibrate it.
    ```
    * Save this file with a `.vtt` extension (e.g., `mysubtitles.vtt`). **Make sure there is a blank line between each subtitle entry.**

### Step 2: Use PodViewer

1.  **Open the [PodViewer App](https://nhaouari.github.io/podviewer/).**
2.  **Upload Audio:** Click the **Audio** button and select your `.mp3` file.
3.  **Upload Subtitles:** Click the **Subtitles** button and select your `.vtt` file.
4.  **Customize Text:**
    * Click on the main title (`PodViewer`) to edit your podcast's title.
    * Click on `Podcast by: Your Name` in the bottom-right to add your credit.
5.  **Prepare to Record:** The player is now ready. Maximize your browser window for the best quality.

### Step 3: Record Your Clip

The final step is to record the PodViewer window as it plays.

1.  **Use a Screen Recorder:**
    * **macOS:** You can use the built-in screen recorder (press `Cmd + Shift + 5`).
    * **Windows:** You can use the snipping tool for recording.
    * **Third-party tools:** OBS Studio or Loom are also great options.
2.  **Start Recording:** Start your screen recording, then click the **Play** button in PodViewer.
3.  **Let it Play:** Allow the audio to play all the way through.
4.  **Stop Recording:** Once finished, stop the screen recording.
5.  **Trim (Optional):** You can use a simple video editor (like iMovie on Mac or Clipchamp on Windows) to trim the start and end of your recording.

You now have a high-quality, perfectly square video clip ready to be shared on your favorite social media platform!

## How to Set Up Locally

This project is a single `index.html` file with no build process, so setup is very simple.

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/your-username/podviewer.git](https://github.com/your-username/podviewer.git)
    ```
2.  **Navigate to the directory:**
    ```sh
    cd podviewer
    ```
3.  **Open in Browser:** Simply open the `index.html` file directly in your web browser.

---

*Built with HTML, Tailwind CSS, and plain JavaScript using Gemini 2.5 Pro*
