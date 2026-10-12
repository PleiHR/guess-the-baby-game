# Guess the Baby

A live game for Plei's All Hands: the host shows baby photos on a shared screen, everyone votes from their phone by scanning a QR code, and results appear on the shared screen when time runs out.

## How to run it

1. Open the game site on the computer you'll share in the call. This is the host screen.
2. In the editor, add each baby photo, write 2 to 6 names, and tick the correct one. Photos and settings are saved in that browser, so run the game from the same computer and browser.
3. Click **Open lobby with QR** and share your screen. People scan the QR, type their name and join.
4. Click **Start**. Each photo has a countdown; when it ends, the results show on screen. Continue to the next photo, then the final leaderboard.

Keep the host tab open during the whole game: phones connect directly to it. The dot in the bottom bar is green when the game is online.

## How it works

- Single static page (`index.html`), hosted on GitHub Pages.
- The host's browser holds the game state. Phones connect to it peer-to-peer with [PeerJS](https://peerjs.com/), using PeerJS's free public signaling server.
- Nobody needs an account to play. Photos never leave the host's browser except to be shown on players' phones during the game; they are not stored in this repository.
