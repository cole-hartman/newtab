# New Tab Clock

A dark new-tab clock with Instrument Serif and Motion digit transitions.

## Use as your Chrome new tab

New Tab Redirect loads an intermediate extension page before opening this site.
Installing this folder directly as a new-tab extension removes that redirect and
loads the clock, font, and animation library from your computer.

1. Open `chrome://extensions` in Chrome.
2. Turn on **Developer mode**.
3. Choose **Load unpacked** and select this folder (the one containing `manifest.json`).
4. Open a new tab and choose **Keep it** if Chrome asks about the new-tab change.
5. Disable **New Tab Redirect** if Chrome continues to use it.

This extension requests no browser or website permissions. It makes no network
requests and works offline. The ordinary website and local preview still work.
Chrome controls any blank frame before the extension document begins loading;
this removes the redirect, but cannot guarantee every Chrome version paints
its first frame dark.

To undo the change, remove **New Tab Clock** from `chrome://extensions` and
re-enable **New Tab Redirect** if desired.

## Local website preview

Run `python3 -m http.server 8000 --bind 127.0.0.1` from this folder and open
<http://127.0.0.1:8000>.

## Dependencies

- Motion 14.14.0: `vendor/motion-14.14.0.js` (MIT license alongside).
- Instrument Serif: `fonts/instrument-serif-regular.ttf` (SIL Open Font License alongside).
