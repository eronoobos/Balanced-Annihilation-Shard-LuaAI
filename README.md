# Balanced-Annihilation-Shard-LuaAI

## [ShardSpringLua](https://github.com/eronoobos/ShardSpringLua) configuration for [Balanced Annihilation](http://imolarpg.dyndns.org/trac/balatest/) as a [Spring](https://github.com/spring/spring) mod dependency.

### Basic Information

This is a Spring mod archive that Balanced Annihilation may put in its dependencies. This is only the configuration for Balanced Annihilation. To run the AI, Balanced Annihilation must also include the [Shard Lua AI base](https://github.com/eronoobos/ShardSpringLua).

### Installation

Clone this repository into a Spring archive directory in its games directory. `--recursive` must be used to get [the submodule that contains the configuration](https://github.com/eronoobos/BABAR-The-Shardifant).
```
git clone --recursive https://github.com/eronoobos/ShardSpringLua.git ~/.spring/games/Balanced-Annihilation-Shard-LuaAI.sdd
```

Checkout Balanced Annihilation via SVN into a Spring archive directory:
```
svn checkout http://imolarpg.dyndns.org/svn/trunk ~/.spring/games/BA.sdd
```

or

Extract Balanced Annihilation from the latest archive on springfiles.com (at time of writing, [version 9.35](http://springfiles.com/spring/games/balanced-annihilation-84)) into a Spring archive directory.

In BA.sdd/modinfo.lua add this mod as a dependency and change Balanced Annihilation's version to "shard" or something else, to differenciate it from the unmodified game version:
```
return {
  name='Balanced Annihilation',
  description='Balanced Annihilation',
  shortname='BA',
  version='shard',
  mutator='Official',
  game='Total Annihilation',
  shortGame='TA',
  modtype=1,
  depend = {
    "Shard LuaAI $VERSION",
    "Balanced Annihilation Shard LuaAI $VERSION",        
  },
}
```

The first dependency line, `"Shard LuaAI $VERSION"`, is the Shard Lua AI base, which must be cloned into place:
```
git clone https://github.com/eronoobos/ShardSpringLua.git ~/.spring/games/ShardSpringLua.sdd
```

To resulting AI can be found in Spring lobbies under the name "ShardLua <not-versioned>".