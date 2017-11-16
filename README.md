Bowling Kata
============

Based from [Uncle Bobs Bowling Game Kata](http://butunclebob.com/ArticleS.UncleBob.TheBowlingGameKata).

Getting Started
---------------

```bash
$ composer install
$ vendor/bin/phpspec describe Game
```

Rules
-----

- The game consists of 10 frames
- In each frame the player has 2 opportunities to knock down 10 pins
- The score for the frame is: `total number of pins knocked down` +  `bonuses` (for strikes and spares).
- A **spare** is when the player knocks down all 10 pins in two tries. 
- A **strike** is when the player knocks down all 10 pins on his first try
- The bonus for a **strike** is the score from the next two balls.
- The bonus for a **spare** is the score from the next ball only

In the tenth frame a player who rolls a spare or strike is allowed to roll the extra
balls to complete the frame.  However no more than three balls can be rolled in
tenth frame.

Examples
--------

- I score 0 if I roll 0 20 times, 
- I score 20 if I roll 1 20 times, 
- I score 10 if I roll a spare
- I score 10 if I roll a strike
- I score 15 if I roll a spare and then roll 5
- I score 20 if I roll a strike and then roll 5 and 5
- I score 133 if I roll [ 1, 4, 4, 5, 6, 4, 5, 5, 10, 0, 1, 7, 3, 6, 4, 10, 2,
  8, 6]

![Scorecard](https://raw.githubusercontent.com/dantleech/bowling-kata/master/score.png)
