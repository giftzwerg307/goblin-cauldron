# Goblin Cauldron — NIIMBOT B1 prototype

This is an experimental single-page web app for searching MTG tokens via Scryfall, previewing a compact 50 x 30 mm label, and sending it to a NIIMBOT B1 through a community Web Bluetooth driver.

## iPhone-only setup (no Mac/Xcode)
1. Unzip this folder.
2. Host `index.html` on a secure HTTPS static host (for example, a GitHub Pages repository). Web Bluetooth does not work from a `file://` URL, and iOS Safari does not expose Web Bluetooth.
3. Open the HTTPS page in a compatible iOS browser such as Bluefy that exposes Web Bluetooth. Keep internet access on for Scryfall and the printer driver script.
4. Power on the B1, insert labels, connect, search/select a token, inspect the preview, then print one test label.

## Important limitations
- This is a prototype, not a native iOS app. It relies on an externally hosted NIIMBOT driver script and Scryfall API/image URLs.
- Web Speech recognition may not work in the chosen iOS browser. The search field and iOS keyboard dictation are the fallback.
- 50 x 30 mm is a starting geometry. Actual stock and label orientation need calibration. The illustration is approximated by cropping the card image; small print may not remain legible on a thermal label.
- Always test one copy before printing a batch. This project is unofficial and not affiliated with Wizards of the Coast or NIIMBOT.
