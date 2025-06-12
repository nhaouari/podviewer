Of course! Based on the provided code, here is a comprehensive `README.md` file for the PodViewer project.

---

# PodViewer 🎧✨

**A dynamic, browser-based player for creating captivating audiograms with kinetic typography, image overlays, and audio-reactive visuals. All from a single HTML file.**

PodViewer transforms standard audio and subtitle files into an engaging visual experience, perfect for sharing podcast clips, audio snippets, or narrated stories on social media.


*(A sample screenshot demonstrating the player interface with kinetic text and a dynamic background.)*

---

## 🚀 Key Features

*   **Synchronized Playback:** Flawlessly syncs an audio file (`.mp3`, `.wav`, `.ogg`) with a WebVTT subtitle file (`.vtt`).
*   **Kinetic Typography Engine:** Bring words to life! The player supports word-by-word highlighting with a rich library of animations, all controlled via simple tags in your VTT file.
    *   Animations include: `shake`, `pulse`, `wave`, `zoom-in`, `slide-up`, `glitch`, `glow`, and more.
    *   Special effects for hierarchical titles (`title1`, `title2`, `title3`) and underlines (`subline`).
    *   A full-line `typing` effect for a classic "live typing" feel.
*   **Dynamic Audio Visualization:** A generative, audio-reactive background that pulses and shifts with the beat of your audio. The mood and color palette can be controlled directly from the VTT file.
*   **Image & GIF Support:** Display static images or animated GIFs at specific moments by adding a simple `<img:...>` tag to your subtitles.
*   **Advanced VTT Editor:**
    *   Powered by **Monaco Editor** (the engine behind VS Code) for a professional editing experience.
    *   **Focus Mode:** Isolates the currently playing subtitle cue in the editor, allowing you to make live edits without distraction.
    *   **Live Reload:** Changes made in the editor are reflected in the player in real-time.
*   **Easy Image Integration:** Upload images or **paste them directly from your clipboard** into the editor. The app handles the Base64 conversion and embeds the image seamlessly.
*   **Live Customization Panel:** Fine-tune the experience on the fly with a comprehensive settings modal.
    *   Adjust font family, size, and highlight timing.
    *   Toggle kinetic effects, image visibility, and background blur.
    *   Switch to **RTL mode** for right-to-left languages like Arabic.
*   **Zero Dependencies & Portable:** Everything is packed into a **single `index.html` file**. No build process, no server needed. Just open it in your browser.

---

## 🛠️ How to Use

1.  **Open the File:** Open [Link](nhaouari.github.io/podviewer/).
2.  **Upload Audio:** Click the "Audio" button and select your `.mp3`, `.wav`, or `.ogg` file.
3.  **Upload Subtitles:** Click the "Subtitles" button and select your `.vtt` file (see syntax below).
4.  **Play!** Press the play button to see the magic happen.
5.  **Customize (Optional):**
    *   Click the **Settings (⚙️)** icon to open the live settings panel and adjust the look and feel.
    *   Toggle **Advanced Mode** in the settings to open the live VTT editor.
    *   In Advanced Mode, toggle **Editor Focus Mode** to easily edit the text for the current audio segment.

---

## ✨ The VTT Magic: Syntax Guide

PodViewer extends the standard VTT format with custom tags to control the visual effects.

### Basic Cue

This is a standard VTT cue. The text will appear with word-by-word highlighting.

```vtt
WEBVTT

00:00:05.000 --> 00:00:08.500
This is a standard line of text.
```

### Kinetic Word Effects `<fx:...>`

Wrap a word or phrase in an `<fx:...>` tag to apply a specific animation when it's highlighted.

```vtt
00:00:09.000 --> 00:00:12.000
This text will <fx:pulse>pulse</fx:pulse> and this will <fx:shake>shake</fx:shake>.
```

**Available Effects:** `shake`, `pulse`, `wave`, `zoom-in`, `slide-up`, `glitch`, `fade-in`, `glow`, `subline`.

### Title & Heading Effects

Use these for more prominent, stylized text.

```vtt
00:00:13.000 --> 00:00:16.000
<fx:title1>THIS IS A MAJOR HEADING</fx:title1>

00:00:17.000 --> 00:00:20.000
<fx:title2>A Slightly Smaller Subheading</fx:title2>
```

### Typing Effect

The `<fx:typing>` tag applies to the entire line. The text will be revealed character by character over the duration of the cue.

```vtt
00:00:21.000 --> 00:00:26.000
<fx:typing>This entire line will be typed out live.</fx:typing>
```

### Displaying Images `<img:...>`

Use the `<img:...>` tag to display an image or GIF. The subtitle text will be hidden for the duration of this cue.

- **Using an external URL:**
  ```vtt
  00:00:27.000 --> 00:00:31.000
  <img:https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjEx.../giphy.gif>
  ```
- **Using an uploaded/pasted image:**
  When you upload or paste an image, the editor inserts a tag with a local reference.
  ```vtt
  00:00:32.000 --> 00:00:36.000
  <img:pasted_image_1678886400000.png>
  ```
- **Adding an effect to an image:**
  ```vtt
  00:00:37.000 --> 00:00:42.000
  <img:my_image.jpg,fx:slow-zoom-in>
  ```

### Controlling Background Mood `<mood:...>`

Add a `<mood:...>` tag at the beginning of a cue's text to change the color palette and behavior of the audio-reactive background.

```vtt
00:00:43.000 --> 00:00:48.000
<mood:angry>Now the tone has shifted, and the background will be red and chaotic.

00:00:49.000 --> 00:00:54.000
<mood:calm,0.99>This part is very calm. The second value (0.99) makes particles appear less frequently.
```

**Available Moods:** `default`, `angry`, `calm`, `happy`, `sad`.

---

## 💻 Built With

*   **HTML5**
*   **Tailwind CSS** - For rapid, utility-first UI development.
*   **Vanilla JavaScript (ES6+)** - No frameworks, just modern JS.
*   **Web Audio API** - For the dynamic, audio-reactive background visualization.
*   **Monaco Editor** - The editor that powers VS Code, for a first-class VTT editing experience.

---

## 🔮 Future Ideas

- [ ] **Video Export:** The most requested feature! Implement recording the canvas animation to an `.mp4` or `.webm` file using `MediaRecorder` API.
- [ ] **UI for Effects:** A user-friendly interface to add kinetic effects instead of requiring manual VTT tag editing.
- [ ] **Save/Load Project:** Save the current state (audio, VTT, settings) to a local file and load it back later.
- [ ] **More Effects & Transitions:** Expand the library of kinetic text animations and add transitions between image/text cues.
- [ ] **Waveform Display:** Add an optional audio waveform visualizer to the UI.