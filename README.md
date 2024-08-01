# tic-tac-toe-move

This is a simple tic-tac-toe game built with Move. It is a simple command line game that allows two players to play tic-tac-toe.

# Publish the module

To publish the module, run the following command:

```bash
aptos init --profile game --network devnet
aptos move publish --named-addresses deploy_account=game --profile game
```

# Run the module

## Setup

Create 2 accounts for the players:

```bash
aptos init --profile x --network devnet
aptos init --profile o --network devnet
```

## Play moves

This is the board layout:

```
|-|-|-|
|0|1|2|
|-|-|-|
|3|4|5|
|-|-|-|
|6|7|8|
|-|-|-|
```

To play a move, run the following command:

```bash
aptos move run --function-id game::tic_tac_toe::play_space --args address:game u64:5 --profile x
```

This will play the move `x` at space `5`.

## Other commands

Please refer to the source code for other commands.