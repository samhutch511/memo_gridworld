# A gridworld for memo

A teaching notebook for [memo](https://github.com/kach/memo), a language for modelling how people reason about each other.

Alice walks through a small town to buy snacks, and her friend Bob watches. Four things may or may not be true that day: Main Street may be closed, Alice may need cash, west mart may be closed, and the bank may be on strike. Alice knows which are true. Bob doesn't, and has to work it out from where she goes.

The notebook, [`map.ipynb`](map.ipynb), works through the model in order:

1. Defines the 9×10 town map and draws it, both by tile type and as participants in the original experiment saw it.
2. Builds the movement rules and uses memo to model how Alice plans her route (`alice_Q`), how Bob predicts her next move (`bob_guesses_move`), and how Bob infers which conditions hold after seeing a move (`bob_guesses_model`).
3. Lets you define your own scenario, with a starting square and the four conditions, and draws Alice's route.
4. Replays that scenario interactively. Click along Alice's route to see Bob's predictions of her next move and his beliefs about the world, step by step.

## Setup

Use Python 3.12 or later.

```bash
pip install -r requirements.txt
jupyter lab map.ipynb
```

Run the cells from top to bottom. The whole notebook takes well under a minute. The last cell is interactive and needs `ipympl`, which is in `requirements.txt`.

## Contents

```
map.ipynb   the notebook
img/        emoji pictures used to draw the map
```
