---
name: quote-part
description: Instant Make Parts Now quote for a CAD file (STL, STEP, 3MF, OBJ) - 3D printing (SLS nylon, FDM) or CNC machining (aluminum, brass) - with the price and ship date for each speed.
---

Quote a part with Make Parts Now, following the quote-parts skill of this plugin. The user's message with this command names the CAD file and may give a quantity and options (material, color, finish, speed) in their own words.

1. The CAD file is a path in this workspace, an @-mentioned file, or a public https link. If no file was given, ask for one. If no quantity was given, ask for it.
2. For an https link, call `quote_part` with it as `file_url`. For a local file, call `create_upload_link` with the file name and PUT that one file's raw bytes to `put_url` in the terminal (`curl -sS -T "<path>" "<put_url>"`), then call `quote_part` with `upload_id`. Upload only that CAD file, never any other file.
3. Pass only the options the user named, in their own words.
4. Show the `summary` line first, then each speed's total and estimated ship date, and `quote_url`. Offer to change the quote or create a checkout link; never order or pay without the user choosing a speed.
