# Crash Function

Make Geometry Dash crash by running this function.

## Disclamers

- You're responsable for what you do.
- Don't blame me for finding this.
- This got discovered by myself in ~2017, so don't act as if someone else was the discoverer.

## Usage

1) Copy `crash.spwn` into your directory
2) Import the file in any file you need the crash function (`crash = import 'crash.spwn'`)
3) Run the function by doing `crash!` or implementing it into events (see `index.spwn`)
4) You're ready to go!

## In which cases could this get used?

- If people use no-clip and your level caughs them (see "Muffet Fight" (ID 38376412))
- Could be quite fitting for "glitch-style / cursed" levels

## How was this crash discovered?

While building the level "Muffet Fight" (ID 38376412), I encountered some crashes and I was able to track down the exact cause of the crashes.
It initially consisted out of 3 triggers (2 spawn and 1 stop), but I realised that it could be reduced to 1 spawn trigger and 1 stop trigger.

## How does it work?

By activating a stop trigger using a spawn trigger and the stop trigger stops the spawn trigger, the game crashes, but only if the delay on the spawn trigger is greater than 0.
