# Line Scan Camera

A "poor man's" finish-line camera. Point it at the line, and instead of
recording normal video, it builds one continuously-growing image out of a
single thin vertical slice of each frame — the same underlying idea as a real
photo-finish (slit-scan) camera, just built from ~30 ordinary video frames a
second instead of a true high-speed sensor.

**Honest limitation:** time resolution is capped at roughly 1/30th of a
second per slice — noticeably coarser than real photo-finish gear. Good for
casual use (practice, away meets without your real equipment) where you don't
need hundredth-of-a-second precision. Not a replacement for FinishLynx.

## How to use it

1. Open the app, allow camera access, point the phone at the finish line.
2. A red vertical line appears over the live camera view — drag it left/right
   until it sits exactly on the actual finish line in frame.
3. Tap **Start Scan**. The screen switches to the growing scan image, with a
   small live camera preview (with the same red line marked) in the corner so
   you can still see runners approaching.
4. Tap **Stop** whenever you're done — after the last finisher, or whenever.
5. You'll see the finished image. **Share** or **Save to device** to keep it,
   or **New scan** to start over for the next race.

Reading the result: the image scrolls left-to-right over time, so anyone
who crossed the line is frozen at the horizontal position corresponding to
when they crossed — read left-to-right for finish order, same as a real
photo-finish strip.

## Deploying to GitHub Pages

Same process as Stopwatch Video:

1. Create a new **public** GitHub repository (e.g. `line-scan-camera`).
2. Upload all files here, keeping the `icons/` folder structure intact.
3. Repo **Settings → Pages** → Source: `Deploy from a branch`, branch `main`,
   folder `/ (root)`. Save.
4. Wait a minute or two for the live URL, e.g.
   `https://yourusername.github.io/line-scan-camera/`
5. Open that URL in Chrome on Android, then **Add to Home Screen** to install
   it as a real app icon.

## Known limitations (first version)

- Time resolution ≈ 1/30th of a second per slice (camera frame rate dependent).
- Finish-line position is set once per scan — if the camera moves, the line
  moves with the frame, not with the real world.
- Very long scans (many minutes) use more memory as the image grows; fine for
  a single race, less ideal for hours of continuous use.
- This hasn't been tested on a real device yet — try it out and report back
  anything that feels off.
