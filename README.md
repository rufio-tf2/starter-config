# Starter Config

The config that I use it too complicated for the average person's needs. If all you want to do is create an [Uber Bind](https://youtu.be/a8yKrKD1EJg) and/or a [Rocket Jump Script](https://youtu.be/mwGKUsq1fTM), this is probably all you need.

## Install

1. [Download](https://github.com/rufio-tf2/starter-config/archive/master.zip) this repo
1. Unzip it
1. If your folder structure is `starter-config-master/starter-config-master` save the inner folder and delete the outer folder
1. Move the remaining folder into your `tf/custom` folder
1. Navigate into the `cfg` folder: `tf/custom/starter-config-master/cfg` to add your configurations
1. Feel free to rename `starter-config-master`

## Configure things

### Examples

#### Rocket Jump Script

1. Navigate into the `cfg` folder installed above: `tf/custom/starter-config-master/cfg`
1. Open `soldier.cfg`
1. Below the line that says `exec allclass`, add:

   ```
   alias +rocketJump "+jump; +duck; +attack;"
   alias -rocketJump "-jump; -duck; -attack;"
   bind KEY +rocketJump
   ```

1. Change `KEY` to be whatever key you want to use for the rocket jump script
1. Open `reset.cfg`, and reset the `KEY` to its default command (look [here](https://wiki.teamfortress.com/wiki/List_of_default_keys)). For example, if you used `MOUSE2` (right-click) for the rocket jump script, you should add this:

   ```
   bind MOUSE2 +attack2
   ```

1. Restart TF2

#### Uber Bind

1. Navigate into the `cfg` folder installed above: `tf/custom/starter-config-master/cfg`
1. Open `medic.cfg`
1. Below the line that says `exec allclass`, add:

   ```
   alias alertUber "say_team UBER POPPED!!!!!"
   alias +alertAndPopUber "+attack2; alertUber;"
   alias -alertAndPopUber "-attack2;"
   bind MOUSE2 +alertAndPopUber
   ```

1. Open `reset.cfg`, and reset `MOUSE2` to its default command:

   ```
   bind MOUSE2 +attack2
   ```

1. Restart TF2
