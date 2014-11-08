# Extremely Efficient Engineers

Factories and Fabricators have minimal energy cost.

This mod is part of the Dynamic Energy experiment.  Right now in vanilla metal and energy feel kind of the same.

## Indictments

### Most energy is spent to spend metal.

Fabricators and factories are the biggest energy consumers.  Both of these things are already limited by metal usage.  Attacking either resource has exactly the same effect: the player's build rate slows. 

The mod drastically reduces fabrication energy, and might remove it if the engine ever supports build rates that are not affected by energy efficiency.

### Demand is constant.

Factories are always on and fabbers are usually fabbing.  Storage is a mostly forgotten vestige of the TA heritage; a player who builds one in competitive play gets asked about the unusual move in interviews.

I expect that this mod will be combined with another that adds a different significant use for energy, and one that is more variable, making energy storage valuable. Or you could play a game where energy is basically irrelevant.

## Development

The generated project includes a `package.json` that lists the dependencies, but you'll need to run `npm install` to download them.

PA will upload **all files** in the mod directory, including `node_modules` and maybe even `.git` - you probably don't want to use this in `server_mods` directly, unless you really like waiting.  The template is set up run to run as a project within a peer directory of `server_mods` - I use `server_mods_dev/mod_name`.  The task `grunt copy:mod` will copy the mod files to `../../server_mods/identifier`, you can change the `modPath` in the Gruntfile if you want to run it from somewhere else.

### Available Tasks

- copy:mod - copy the mod files into server_mods
- proc - Proc: read one or more files from PA and munge into one in the mod.
- default: proc, copy:mod
