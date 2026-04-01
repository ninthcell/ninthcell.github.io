---
title: "Game design is the hell I wished for"
date: 2026-04-01
---
I spent a month prototyping an action game. I went through 9 versions. The one thing I was sure would never change — the core concept itself — was the first thing that had to go.

It started with a simple desire: I love the tension of setting up a T-spin in Tetris. That moment where you're risking death to build toward a devastating payoff. I wanted to feel that tension in a shoot-'em-up.

So I started gluing the two games together.

## v1: Tetris + Shmup, side by side

You play a shmup. Armored enemies are immune to your shots. Switch to Tetris anytime — each line clear deals armor-breaking damage.

![Early sketchbook prototype](/assets/posts/game-design-hell/Pasted image 20260401091645.png)
<p class="caption">(Early sketchbook prototype)</p>

**What went wrong:** Once I switched to Tetris, I didn't want to go back. Tetris was fun and complete on its own. The game wasn't greater than the sum of its parts.

## v2: Tetris as a "super" ability

I shrunk the Tetris board to 4x20, limited each session to 7 pieces, and gated entry behind an energy meter. The idea: Tetris should feel like a bomb, not a second game.

<video src="/assets/posts/game-design-hell/v2.webm" controls loop playsinline></video>

**What went wrong:** It was actually worse. A bomb is supposed to release tension — but Tetris requires its own loop of accumulation and release. The "super" felt like homework.

## v3: Tetris as "reload"

This was the first version where both games shared a single tension loop.

The shmup gives you limited ammo. Reloading means dropping a penalty block on the Tetris board, dragging you closer to top-out (game over). But if you clear a line while reloading, you get a temporary attack boost — and buy yourself breathing room.

On top of that, clearing a garbage row at the exact moment it spawns lets you "parry" the enemy bullet back as massive damage.

<video src="/assets/posts/game-design-hell/v3.5.webm" controls loop playsinline></video>

**What went wrong:** Two things. First, the arrow keys controlled both the Tetris piece and the ship — I kept getting hit right after switching back. Second, the parry rewarded the safest state (clean board, first row exposed), not the riskiest. A parry should be a comeback mechanic, not a snowball mechanic.

## v4–5: Stripping the puzzle down

I reduced the board to 2 columns, assigned a button per column, and freed the arrow keys for ship movement only. I also added a visual metaphor: the puzzle board is a bullet-manufacturing factory-gun.

<video src="/assets/posts/game-design-hell/DoubleLine.webm" controls loop playsinline></video>
<p class="caption">(Visual prototype of the factory-gun metaphor)</p>

<video src="/assets/posts/game-design-hell/v4 1.webm" controls loop playsinline></video>

**What went wrong:** The puzzle was now so simple it required no skill. No skill, no tension. The reload became a chore.

## v6: Letting go of Tetris

At this point I went back to the original question: what did I actually love about Tetris? Not the blocks. Not the grid. The *tension curve* — risking death to set up a devastating payoff.

That curve doesn't require a block-stacking puzzle.

So the new mechanic: you dash into enemy bullets to collect them and fill your magazine. Each shot you land temporarily increases your magazine's maximum capacity — so you're rewarded for staying aggressive. The more you stay in danger during a dash, the more you collect. If you collect 20+ bullets in one dash, your gun overloads for a few seconds, making you vulnerable — then dumps everything at once. The damage scales geometrically to the number of bullets collected.

This is the same tension curve as setting up a T-spin: you deliberately put yourself at risk, accumulate toward a threshold, and get a devastating payoff if you survive.

![Prototype render in Blender](/assets/posts/game-design-hell/1_overview.png)
<p class="caption">(Prototype render in Blender)</p>

<video src="/assets/posts/game-design-hell/v6.3.webm" controls loop playsinline></video>

The core concept I started with — Tetris — was completely distilled away. What remained was the tension curve I loved, wearing a completely different skin.

## What's next

This is not the final design. Dash spamming is overpowered, and visual feedback needs work. I'm testing a few more radical changes to solve these problems while keeping the core motivation. But I have a feeling the system has entered a phase of convergence — I'm now thinking about adding patterns, stages, and player weapons like a minigun, a sword, and a bow.

## The hell I wished for

Looking back, the stacking puzzle could have been ditched right after v1. The evidence was already there: Tetris was too captivating on its own, pulling the player away from the action game entirely.

But I don't think I would have arrived at v6 without the obsession. Precisely because I refused to let go of Tetris, I was forced to explore every possible way to make it work inside a shmup — as a second game, as a super, as a reload, as a two-column minigame. Each attempt stripped the puzzle down further, and each failure taught me what I actually cared about. By the time I finally let go of the blocks, I wasn't giving up. I had explored the constraint so thoroughly that the next idea — dash into bullets, accumulate, overload — emerged naturally from everything I'd already tried.

If a colleague had told me to ditch Tetris after v1, I might have listened. But I wouldn't have known *why* I loved it enough to find a different way to keep it.

Solo development is tough. I tested 9 versions in one month. Every step felt like walking through fire. But this pace was only possible because I was solo — when the reason for a change was clear, I could write down the problem, contemplate the fix, and move on without convincing anyone but myself. It may have required more iterations because I am solo. Perhaps this is the hell I wished for.

<p class="note">If you want to see what comes next, I'm at <a href="https://x.com/ninthcellstudio">@ninthcellstudio</a>.</p>
