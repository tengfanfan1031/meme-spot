# 找不同大賽 Spot the Difference

A group spot-the-difference game for team lunches. One computer hosts on the TV; up to about 60 colleagues join on their phones by scanning a QR code. A full game takes up to about 9 minutes (usually less, because a round ends as soon as everyone is done).

**Play:** https://tengfanfan1031.github.io/meme-spot/

## How it works

- 8 geometric pictures, easy to hard: Bauhaus poster, Mondrian grid, low-poly mountains, isometric city, night skyline, Memphis pattern, patterned tiles and a mandala. Each has **3 differences**, kept well apart from each other.
- Everyone plays the same round at the same time on their own phone. Each round lasts up to 60 seconds and ends early once everybody is done.
- Score per round: 100 per difference found, plus a speed bonus (up to 500) for finding all 3. Taps count over a generous area around each difference; a wrong tap freezes you for 3 seconds.
- The TV shows the pictures, a live progress board, who finished fastest, the answers after each round, the overall leaderboard, and a podium at the end.
- The interface is bilingual (Traditional Chinese and English). The pictures are drawn in code (SVG) and contain no text.

## Running a game

1. On the computer connected to the TV, open the link and press **電視主持 Host on TV**.
2. Colleagues scan the QR code on the TV (or open the link and type the room code), enter a name and tap **加入 Join**.
3. When everyone is in, press **開始遊戲 Start game** on the TV (or press Space).
4. Between rounds the TV moves on automatically after 8 seconds; **下一關 Next** skips ahead and **暫停 Pause** holds the answer screen.

Don't refresh the TV page during a game: the room lives in that browser tab. If a phone locks or drops off Wi-Fi, it reconnects automatically and keeps its score.

**自己練習 Practice solo** lets one person play all 8 rounds alone.

## Tech

A single `index.html`; no server, accounts or image files. Networking uses [PeerJS](https://peerjs.com/) (WebRTC): every phone connects directly to the TV browser, which acts as the referee. The QR code uses [qrcodejs](https://github.com/davidshimjs/qrcodejs).

For development, add `#preview=3` to the URL to see round 3 with its differences circled.
