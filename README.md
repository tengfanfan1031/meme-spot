# Meme Spot Duel

A two-player, head-to-head spot-the-difference race for team lunches. Cast it to a TV so everyone can watch.

**Play:** https://tengfanfan1031.github.io/meme-spot-duel--mini-game/

## How it works

- 10 levels, each with a pair of meme pictures and 5 differences, from easy to hard (levels 1–2 are a warm-up, 9–10 are insane).
- Both players see the same pair. **Whoever taps a difference first gets the point**, and it shows up on the other player's screen right away.
- Tap either picture. A wrong tap freezes you for 2 seconds.
- Each level has a time limit (60–90 s). When time runs out, the missed differences are circled in yellow.
- Highest total wins. On a tie, fewer misses wins.
- Each level has 6 possible differences and every match picks 5 at random, so rematches are not identical.

Memes: Doge, Moo Deng, This Is Fine, Capybara Spa, Chill Guy, Woman Yelling at Cat, Two Buttons, Distracted Boyfriend, Stonks, Vibing DJ Cat. All pictures are original SVG tributes drawn from scratch, not the original images.

## Start a match

1. Both players open the link on their phones and enter a name.
2. One player taps **Create room** and shares the 4-character code.
3. The other enters the code and taps **Join**.
4. Both tap **I'm ready** and a 3-second countdown begins.

You can also tap **Practice solo** to play alone.

## Show the match on a TV

1. Open the link on the computer (or TV browser) connected to the TV.
2. Enter the room code and tap **Watch on TV**.
3. The TV shows both pictures side by side, the scores, the timer, who found each difference (blue circle = player 1, pink circle = player 2), misses as red crosses, and the winner.

Several TV views can watch the same room.

## Tech

A single `index.html` with no server or accounts. Multiplayer uses [PeerJS](https://peerjs.com/) (WebRTC) to connect browsers directly. The host's phone acts as the referee and decides who tapped first.

For development, add `#preview=3` to the URL to see level 3's two pictures with all 6 possible differences circled.
