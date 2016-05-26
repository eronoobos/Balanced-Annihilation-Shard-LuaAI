# Balanced-Annihilation-Shard-LuaAI

## [ShardSpringLua](https://github.com/eronoobos/ShardSpringLua) configuration for [Balanced Annihilation](http://imolarpg.dyndns.org/trac/balatest/) as a [Spring](https://github.com/spring/spring) mod dependency.

### Basic Information

This is a Spring mod archive that Balanced Annihilation may put in its dependencies. This is only the configuration for Balanced Annihilation. To run the AI, Balanced Annihilation must also include the [Shard Lua AI base](https://github.com/eronoobos/ShardSpringLua).

### How To

Clone this repository into a Spring archive in its games directory.
```
git clone https://github.com/eronoobos/ShardSpringLua.git ~/.spring/games/Balanced-Annihilation-Shard-LuaAI.sdd
```

Add this mod as a dependency to Balanced Annihilation's modinfo.lua.
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

The first dependency line, `"Shard LuaAI $VERSION"`, is the Shard Lua AI base.