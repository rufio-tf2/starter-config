# Starter Config

If all you want to do is create an [Uber Bind](https://youtu.be/a8yKrKD1EJg) and/or a [Rocket Jump Script](https://youtu.be/T0nc-jepGVw), this is the config you should use.

## Install

1. [Download the ZIP](https://github.com/rufio-tf2/starter-config/archive/master.zip)
1. Unzip it
1. If your folder structure is `starter-config-master/starter-config-master` save the inner folder and delete the outer folder
1. Move the remaining `starter-config-master` folder into your `tf/custom` folder
1. Navigate into the `cfg` folder (`tf/custom/starter-config-master/cfg`) to add your configurations
1. Feel free to rename `starter-config-master`

## Example of how to use

### Rocket Jump Script

1. Navigate into the `cfg` folder installed above: `tf/custom/starter-config-master/cfg`
1. Open `soldier.cfg`
1. Below the line that says `exec reset`, uncomment the lines (remove the `//` slashes):

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

### Uber Bind

1. Navigate into the `cfg` folder installed above: `tf/custom/starter-config-master/cfg`
1. Open `medic.cfg`
1. Below the line that says `exec reset`, uncomment the lines (remove the `//` slashes):

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

### `autoexec.cfg`

The `autoexec.cfg` file is automatically run by TF2 when the game loads. People use this file for FPS configs, and other game configurations that only need to run once when the game loads.

You can only have one `autoexec.cfg` file. If you already have an FPS config and you're using this config for the class files, my recommendation would be to integrate your FPS config into this config by renaming the other configs' `autoexec.cfg` files to anything else, and then having this config's `autoexec.cfg` load the files that you renamed. The game loads this one `autoexec.cfg` file, and that file in turn loads any others that you need. Here's an example of how I did that with Comanglia's FPS config:

https://github.com/rufio-tf2/comanglia-with-class-config
