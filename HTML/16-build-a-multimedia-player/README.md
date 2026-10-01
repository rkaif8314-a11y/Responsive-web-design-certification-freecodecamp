# Responsive Web Design — HTML Series #16: Build a Multimedia Player

This exercise builds a multimedia player using HTML5 audio and video elements, source files, subtitles, and a transcript section.

## Files

- `index.html` — Complete multimedia player.
- `README.md` — Detailed explanation and revision notes.

## 1. Page Structure

The page uses the standard HTML5 structure:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    ...
  </head>
  <body>
    ...
  </body>
</html>
```

The visible content is placed inside a semantic `<main>` element.

## 2. Audio Player

The audio player uses:

```html
<audio controls aria-label="Music player">
  <source
    src="..."
    type="audio/mpeg"
  />
</audio>
```

### `<audio>`

The `audio` element embeds sound content directly into an HTML page.

### `controls`

The `controls` attribute tells the browser to display built-in playback controls such as play, pause, and volume.

### `<source>`

The `source` element specifies the actual audio file.

Important attributes:

- `src` — location of the audio file.
- `type="audio/mpeg"` — tells the browser that the source is an MPEG audio file.

## 3. Accessible Audio Label

The audio player has:

```html
aria-label="Music player"
```

This provides an accessible name for the audio control.

## 4. Video Player

The video section uses:

```html
<video controls width="300" aria-label="Map method video">
  <source
    src="..."
    type="video/mp4"
  />
</video>
```

### Important attributes

- `controls` displays the browser's video controls.
- `width="300"` sets the displayed video width.
- `aria-label` gives the video an accessible description.
- `src` identifies the video file.
- `type="video/mp4"` identifies the MP4 format.

## 5. Captions with `<track>`

The video includes a subtitle track:

```html
<track
  src="..."
  kind="subtitles"
  srclang="en"
  label="English subtitles"
/>
```

### `src`

Specifies the WebVTT subtitle file.

### `kind`

`kind="subtitles"` identifies the track as subtitles.

The original code used:

```html
kind="Video file"
```

That was corrected because `kind` expects a valid track kind such as `subtitles`, `captions`, `descriptions`, `chapters`, or `metadata`.

### `srclang`

Specifies the language of the text track.

```html
srclang="en"
```

means English.

### `label`

Provides the user-facing name of the track:

```html
label="English subtitles"
```

## 6. Transcript Section

A separate transcript section is included:

```html
<section>
  <h2>Transcript</h2>
  <p>This is a video in MP4 format.</p>
</section>
```

The `<section>` groups related content and the `<h2>` identifies the section.

## 7. Fallback Text

The audio and video elements contain fallback text:

```html
Your browser does not support the audio element.
```

and:

```html
Your browser does not support the video element.
```

This text can be shown when a browser cannot handle the corresponding media element.

## 8. HTML Cleanup Applied

Several small validity and quality improvements were made to the submitted code.

### Fixed the heading capitalization

```html
<h1>Multimedia Player</h1>
```

### Fixed the video track kind

Changed:

```html
kind="Video file"
```

to:

```html
kind="subtitles"
```

because `subtitles` is a valid HTML text-track kind.

### Improved the track label

Changed the vague label to:

```html
label="English subtitles"
```

### Fixed the empty video `aria-label`

The original had:

```html
aria-label
```

This was changed to a complete accessible name:

```html
aria-label="Map method video"
```

### Added fallback text

Fallback messages were added inside both media elements.

## Quick Revision Map

| Concept | Example |
|---|---|
| Audio | `<audio>` |
| Audio controls | `controls` |
| Audio source | `<source>` |
| Audio MIME type | `type="audio/mpeg"` |
| Video | `<video>` |
| Video width | `width="300"` |
| Video source | `<source>` |
| Video MIME type | `type="video/mp4"` |
| Subtitles | `<track kind="subtitles">` |
| Track language | `srclang="en"` |
| Track label | `label="English subtitles"` |
| Accessible name | `aria-label` |
| Transcript | `<section>` + `<p>` |

## One-Line Takeaway

**HTML5 multimedia uses `audio`, `video`, `source`, and `track` elements, while captions, labels, and transcripts improve accessibility.**
