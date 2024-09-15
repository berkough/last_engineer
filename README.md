- [The Last Engineer](#the-last-engineer)
  - [About](#about)
  - [Workflow and Structure](#workflow-and-structure)
  - [Roadmap / TODO](#roadmap--todo)
    - [Decision Cyling](#decision-cyling)
    - [Character Disposition](#character-disposition)
    - [Mini Games or Puzzles](#mini-games-or-puzzles)
    - [Inventory](#inventory)

# The Last Engineer

## About

An Atomic Age Retro-Futuristic text adventure game. You play as an engineer who works for the Jovian Oligarchy Oversight Board and you're coming back from a mission on Ganymede. Your ship is low on fuel and you need to stop at the Epsilon-9 space station before heading back to Europa and reporting in about the progress you've made with the Hydro-Mining Consortium. The problem is that Epsilon-9 is abandoned and derelict.

This is a work in progress. This is pre-alpha. But I wanted to use the devlog feature on Itch to document my journey, and now here we are on Github creating a repo for the code because it's starting to become unruly in the Twine editor, and I figured that editing individual files was easier, and I needed the syntax highlighting if I was going to expand the javascript of it all to be more robust.

This is the first time I've ever made a serious attempt to make my own game--I've flirted with the idea, and fiddled around with a bunch of SDKs and IDEs, and full featured engines, and not so full featured engines... That being said, this is also just a proof of concept for myself. I've utilized a number of AI tools to build this, though namely Hotpot's Image generation and some help coming up with ideas and structure for the story from Perplexity. I may or may not dabble with using Chat or Copilot for any code generation.

## Workflow and Structure

I began the project inside of the standard Twine editor, but it became pretty apparent that if I was going to be using the Snowman story format, and trying to do a lot of my own JavaScript coding instead of macros, then I should probably switch to a more modern webdev type of workflow.

Sadly I can't reccomend anything for Node, which is what I wanted to use, but [Tweego](https://www.motoslave.net/tweego/) works really well as an alternative to working with npm dev dependencies. It was also easy enough to setup. I'm working in Debian 12, so for me it was just a matter of downloading and unzipping the archive into my base home directory and putting a symbolic link to the executable in my /usr/local/bin directory.

``` bash
sudo ln -s /home/[username]/tweego/tweego /usr/local/bin/
```

For whatever reason, absolute paths are necessary, otherwise you get an error stating, "too many levels of symbolic links." I have no idea what that means, but eventually I came across a Stack thread that said to use absolute paths, and that solved my problem.

## Roadmap / TODO

### Decision Cyling

I want the player to be able to make different dialog choices based on their own preferences. The narrative will be branching to a certain extent, but will skew heavily toward proof of concept with limited options. Thereby eliminating the overhead of maintaining a story with ever-increasing complexity.

### Character Disposition

Each sub-system on the station will have it's own personality that you get to interact with. I want dialog decisions to affect some of the outcomes. This sort of relates to the decision cyling mechanic, but it will effectively operate in the background, and will not be a system that the player will directly interact with.

### Mini Games or Puzzles

Part of the idea behind the game is that it'll use mini games for each of Epsilon-9's sub-systems. Righ now there is a short blurb on the type of puzzle each room should have, but nothing has been implemented yet.

I'm debating internally how exactly I want to implement the puzzles. I might try a few different ways.

### Inventory

This aspect is partially implemented. It will mainly be used for the datapads scattered throughout the game.