# 找不同大賽 Spot the Difference

A group spot-the-difference game for team lunches. One computer hosts on the TV; up to about 60 colleagues join on their phones by scanning a QR code. A full game takes about 5 minutes.

**Play:** https://tengfanfan1031.github.io/meme-spot/

## How it works

- 8 rounds of real photos, easy to hard. Each round shows two pictures with **3 differences** (picked at random from 6 prepared ones, so replays differ).
- Everyone plays the same round at the same time on their own phone. Rounds last 20–30 seconds and end early once everybody is done.
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

All photos are from Wikimedia Commons and were edited to create the differences (a printed number on a boat, soy sauce packet print and apple stickers were also removed). The edited versions are shared under the same licenses.

1. Harbour Junk — CEphoto, Uwe Aranas, CC BY-SA 3.0
2. Burano Houses — kallerna, CC BY-SA 4.0
3. Beach Umbrellas — Ввласенко, CC BY-SA 3.0
4. Handmade Cups — Terragio67, CC BY-SA 4.0
5. Oil Lamps — Satdeep Gill, CC BY-SA 4.0
6. Sushi Box — Dllu, CC BY-SA 4.0
7. The Peak at Dusk — Estial, CC BY-SA 4.0
8. Apple Pile — Dietmar Rabich, CC BY-SA 4.0

Links to each original are in the game under **相片來源 Photo credits**.

## Tech

A single `index.html` plus the `img/` folder; no server or accounts. Networking uses [PeerJS](https://peerjs.com/) (WebRTC): every phone connects directly to the TV browser, which acts as the referee. The QR code uses [qrcodejs](https://github.com/davidshimjs/qrcodejs).

For development, add `#preview=3` to the URL to see round 3 with all 6 possible differences circled.
