# Chuck-a-Luck

🧪 An open-source implementation of the popular game: Langur Burja.

⚙️ Built using NextJS, RainbowKit, Hardhat, Wagmi, and Typescript.

## What is `Chuck-a-Luck` or `Langur Burja`?

This game has, in fact, many names, like "Jhandi Munda", "Crown & Anchor", etc.

We are presented with a set of symbols on which we can place our bets. 3 to 6, 6-sided dice, each face representing a symbol, are thrown. Now, if:

* none of the symbols we placed bets on appear, we lose our bet
* if one or more symbols appear, then the original bet is returned
* if the symbols repeat across the dice, then the original bet multiplied by the number of occurrences is returned additionally

## Game Setup

This version of the popular game is adapted to work well for
the web3 world.

1. The party master starts a round by choosing the number of dice to play with, the number of rounds, the time limit per round, the minimum stake (min: 0.001ETH), and the quorum to form (minimum 2 players)
2. Wait for players to join the round. Wait time is up to 15 minutes.
3. Before the game begins, each player needs to stake ETH to get luck tokens. This is done within the waiting period.
4. The party master starts the game once the quorum is reached. If quorum fails, then any staked ETH is eligible for claimback.
5. For each round:
  1. Each player places bets on one or more symbols, limited by the number of tokens available. If the player has no tokens or wants to bet with more, then an option to exchange ETH for tokens can be availed.
  2. Players can choose to abstain from placing bets, attracting a penalty of 5% of available tokens.
  3. Players can choose to abandon the game altogether, attracting a penalty of 20% of available tokens.
  4. Once the time limit has elapsed, the dice is rolled [by the game master] and the bets are evaluated.
  5. Each player is rewarded or penalized accordingly.
6. After the rounds are done, the players are given an option to continue (with increased stakes) within 30 seconds. Based on the outcome of the vote, the game respawns or finishes.
7. Once the game completes, players have the ability to claim ETH equivalent to the tokens they possess. Tokens can be carried forward for future games.