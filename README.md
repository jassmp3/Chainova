# CHAINOVA - by Jass

Single self-contained file: `index.html` (music and logo are embedded).
Upload it to any static host (Netlify, Vercel, GitHub Pages, Cloudflare Pages) and open it. No build step.

## Needs internet for
- three.js r128 from cdnjs.cloudflare.com
- Orbitron / Fredoka fonts from Google Fonts

## Important: multiplayer
Rooms use the claude.ai artifact runtime (`claude.use('room')`), which only exists inside a published Claude artifact.
On your own host, single player works fully, but CREATE/ENTER ROOM will show "Multiplayer needs the shared link".
To get multiplayer on your own host, replace the room layer (search `openRoom` in index.html) with a WebSocket relay
(e.g. a small Node `ws` server that forwards messages between clients in the same room code).
Keep the same message names: cfg, ch, kick, start, mv, sk, sh, te, su, pu, pe, ab.

## Other notes
- Chat history is stored in the browser's localStorage.
- "Leave a review" opens https://ig.me/m/jassss.mp3
