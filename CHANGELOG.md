# Version history

## 1.9.2 — November 2026
- **Fixed: no sound in videos made in Safari.** Safari's sound encoder describes its AAC sound in a
  way the MP4 file didn't expect, so players saw "0 channels" and stayed silent. DeepParallax now
  writes the sound description itself.
- **Fixed: slideshows flashing the depth view in Safari.** When a 3D canvas is drawn onto another
  canvas, Safari can hand back the picture from the step before, which was sometimes the depth view
  used to find morph points. Saved frames are now copied directly from the graphics chip's pixels.

## 1.9.1 — November 2026
- **Soundtrack.** Add a music file (MP3, M4A, WAV or AIFF), or drop one onto the preview or the
  side panel. Set the volume, where in the song to start, fade in, fade out, and whether to repeat a
  short song. The music goes into the slideshow video and the Main tab's video, and plays during
  Play all and Quick preview. It is saved as AAC sound inside the MP4.
- **Better automatic morph points.** The near shape's outline is now followed edge to edge, like
  placing points by hand in Morph Lab: 28 points, evenly spaced and numbered in order around both
  shapes, with the numbering turned so point 1 meets its closest match. (Before, points could pair
  with the wrong part of the outline, which folded the picture.) Shapes that fill most of the width
  are now found too, so those morphs are no longer plain dissolves.
- **▶ Preview titles** button on the Text tab plays the slide from the start to show the text
  coming in and going out.
- The finished video on the Slides tab now fits the panel instead of showing at full 4K size.
- Exports use much less memory: scratch pictures are released as soon as each transition ends.
  This is aimed at the flashes and lines seen in some 4K exports in Safari.
- A background tidy-up can no longer change the wrong photo while a slideshow is being drawn.

## 1.9.0 — November 2026
- **▶ Play all** plays the whole slideshow live in the preview, with transitions, titles and the
  fade in and out. Click the preview or press Esc to stop.
- **Automatic morph points.** The morph finds the nearest shape in both pictures (using the depth
  map) and places matching points around its outline, plus points along the horizon. Your own points
  are kept, and any automatic point you drag becomes yours.
- **Layered morph.** "Background follows by" lets the near layer move and dissolve first, with the
  background catching up a moment later.
- The Slides tab now starts with Play all, Transitions and Random moves, above the list of slides.
  The shuffle options are tucked into a "Shuffle options" section.

## 1.8.0 — November 2026
- **Slideshows.** The Batch tab is now the **Slides** tab. Export one slideshow video with
  transitions, or one video per slide.
- **Titles and lower thirds** on every photo (new **Text** tab), with typeface, size, colour, shadow
  and animation choices. Text is drawn sharply on top of the 3D picture.
- **Title cards:** plain cards with words, a colour, gradient or glow background, placed anywhere in
  the show.
- **Transitions**, set separately for each slide: cut, crossfade, fade through black, dip to colour,
  cross-blur, cross zoom, directional wipe, push, slide over, iris, star wipe, clock wipe, and
  **morph** with matching points (after Morph Lab). Random transitions and "use for every slide".
- **Quick preview** of the whole slideshow or of a single transition, at low resolution.
- **Fixed on iPad:** exports failed with "Canvas has no frame". Every frame is now built on an
  ordinary 2D canvas before it becomes video, with a pixel-copy backup. A tip suggests 1080p on
  iPhone and iPad, where 4K often runs out of memory.

## 1.7.2 — November 2026
- **Delete all** button above the batch list.
- Fixed: a deleted photo could reappear in the next batch, because it stayed open in the preview.
  Removing the photo on screen now shows the next one, or clears the preview if none are left.

## 1.7.1 — November 2026
- The repository now opens with a launcher page (`index.html`); the app is `DeepParallax.html`.
- Added an "About and licences" section on the Main tab.
- The Detailed AI model is now labelled "non-commercial use only".

## 1.7.0
- The AI now works in browsers that block downloads from other websites (Edge on iPhone and iPad
  opening a file from Files). The AI's control program is built in, and the two large AI files can
  be chosen by hand once, then kept on the device.

## 1.6.1
- iPhone and iPad: finished videos open a "ready" box with **Save to Photos / Share** instead of a
  download that iOS might block.
- Export batch with an empty batch now uses the open photo.
- Stopped iOS zooming in when a number box is tapped.

## 1.6.0
- In Whole photo framing, the photo's frame now stays fixed and square. Camera moves happen inside
  it and never tilt or move its edges.

## 1.5.1
- Clicking anywhere on a batch row shows that photo.
- One video per photo can be saved as a single ZIP file (one download).

## 1.5.0
- **Batches:** many photos, each with its own move, length, intensity, crop and depth map.
  Shuffle moves at random. Export separate videos or one joined video.
- **Reset all Look settings** button.
- Fixed exports stalling in Safari (the video encoder was being waited on too strictly).
- AI fallback for iPhone and iPad (older-style ONNX Runtime).
- WebGPU self-test before use, and a "Copy a report" button in Browser check.

## 1.4.0
- WebGPU drawing for browsers that have WebGL switched off.

## 1.3.0 – 1.3.1
- Crop edges, "keep the photo's outer edges straight", four turning push/pull moves.
- Backup mode: smoother picture, no more stuck exports.

## 1.2.0
- Backup renderer that needs no graphics chip.

## 1.1.0 – 1.1.2
- Main tab with all the essentials; moves as icon buttons.
- Whole photo framing, drag and pinch to reposition.
- On-screen error messages and Browser check.

## 1.0.0
- First version: AI depth map, parallax camera moves, keyframes, depth of field, look, MP4 export up
  to 4K.
