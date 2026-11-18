# 找不同大賽 Spot the Difference

A group spot-the-difference game for team lunches. One computer hosts on the TV; up to about 60 colleagues join on their phones by scanning a QR code. A full game takes up to about 9 minutes (usually less, because a round ends as soon as everyone is done).

**Play:** https://tengfanfan1031.github.io/meme-spot/

## How it works

- 8 photos of Macau, easy to harder. Each round shows two pictures with **3 differences** (picked at random from 6 prepared ones, so replays differ).
- Everyone plays the same round at the same time on their own phone. Each round lasts up to 60 seconds and ends early once everybody is done.
- Score per round: 100 per difference found, plus a speed bonus (up to 500) for finding all 3. A wrong tap freezes you for 3 seconds.
- The TV shows the pictures, a live progress board, who finished fastest, the answers after each round, the overall leaderboard, and a podium at the end.
- The interface is bilingual (Traditional Chinese and English). The pictures contain no text.

## Running a game

1. On the computer connected to the TV, open the link and press **電視主持 Host on TV**.
2. Colleagues scan the QR code on the TV (or open the link and type the room code), enter a name and tap **加入 Join**.
3. When everyone is in, press **開始遊戲 Start game** on the TV (or press Space).
4. Between rounds the TV moves on automatically after 8 seconds; **下一關 Next** skips ahead and **暫停 Pause** holds the answer screen.

Don't refresh the TV page during a game: the room lives in that browser tab. If a phone locks or drops off Wi-Fi, it reconnects automatically and keeps its score.

**自己練習 Practice solo** lets one person play all 8 rounds alone.

## Photo credits

All photos are from Wikimedia Commons and were edited to create the differences. Any lettering, signs and inscriptions were removed so the pictures contain no text. The edited versions are shared under the same licenses.

1. 龍環葡韻 Taipa Houses — Abasaa, public domain
2. 觀音像 Kun Iam Statue — Diego Delso, CC BY-SA 3.0
3. 嘉模聖母堂 Our Lady of Carmel Church — Yumeto, CC BY-SA 4.0
4. 玫瑰堂 St. Dominic's Church — edwin.11, CC BY 2.0
5. 漁人碼頭 Fisherman's Wharf — Diego Delso, CC BY-SA 3.0
6. 路環市區 Coloane Village — LN9267, CC BY-SA 4.0
7. 議事亭前地 Senado Square — Bahnfrend, CC BY-SA 4.0
8. 大三巴牌坊 Ruins of St. Paul's — AwOiSoAk KaOsIoWa, CC BY-SA 3.0

Links to each original are in the game under **相片來源 Photo credits**.

## Tech

A single `index.html` plus the `img/` folder; no server or accounts. Networking uses [PeerJS](https://peerjs.com/) (WebRTC): every phone connects directly to the TV browser, which acts as the referee. The QR code uses [qrcodejs](https://github.com/davidshimjs/qrcodejs).

For development, add `#preview=3` to the URL to see round 3 with all 6 possible differences circled.
