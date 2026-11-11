# Version history

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
