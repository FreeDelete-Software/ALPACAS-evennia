# API Summary

[evennia](api:evennia) - library root
- [evennia.accounts](api:evennia.accounts) - the out-of-character entities representing players
- [evennia.commands](api:evennia.commands) - handle all inputs. Also includes default commands
- [evennia.comms](api:evennia.comms) - in-game channels and messaging
- [evennia.contrib](api:evennia.contrib) - game-specific tools and code contributed by the community
- [evennia.help](api:evennia.help) - in-game help system
- [evennia.locks](api:evennia.locks) - limiting access to various systems and resources
- [evennia.objects](api:evennia.objects) - all in-game entities, like Rooms, Characters, Exits etc
- [evennia.prototypes](api:evennia.prototypes) - customize entities using dicts
- [evennia.scripts](api:evennia.scripts) - all out-of-character game objects
- [evennia.server](api:evennia.server) - core Server and Portal programs, also network protocols
- [evennia.typeclasses](api:evennia.typeclasses) - core database-python bridge
- [evennia.utils](api:evennia.utils) - lots of useful coding tools and utilities
- [evennia.web](api:evennia.web) - webclient, website and other web resources


## Shortcuts

Evennia's 'flat API' has shortcuts to common tools, available by only importing `evennia`.
The flat API is defined in `__init__.py` [viewable here](github:evennia/__init__.py)


### Main config

- [evennia.settings_default](github:evennia/settings_default.py) - all settings (modify/override in `mygame/server/settings.py`)

### Search functions

- [evennia.search_account](api:evennia.utils.search#evennia.utils.search.search_account)
- [evennia.search_object](api:evennia.utils.search#evennia.utils.search.search_object)
- [evennia.search_object_by_tag](api:evennia.utils.search#evennia.utils.search_object_by_tag)
- [evennia.search_script](api:evennia.utils.search#evennia.utils.search_script)
- [evennia.search_channel](api:evennia.utils.search#evennia.utils.search_channel)
- [evennia.search_message](api:evennia.utils.search#evennia.utils.search_message)
- [evennia.search_help](api:evennia.utils.search#evennia.utils.search.search_help)

### Create functions

- [evennia.create_account](api:evennia.utils.create#evennia.utils.create.create_account)
- [evennia.create_object](api:evennia.utils.create#evennia.utils.create.create_object)
- [evennia.create_script](api:evennia.utils.create#evennia.utils.create.create_script)
- [evennia.create_channel](api:evennia.utils.create#evennia.utils.create.create_channel)
- [evennia.create_help_entry](api:evennia.utils.create#evennia.utils.create.create_help_entry)
- [evennia.create_message](api:evennia.utils.create#evennia.utils.create.create_message)

### Typeclasses

- [evennia.Defaultaccount](api:evennia.accounts.accounts#evennia.accounts.accounts.DefaultAccount) - player account class ([docs](Components/Accounts))
- [evennia.DefaultGuest](api:evennia.accounts.accounts#evennia.accounts.accounts.DefaultGuest) - base guest account class
- [evennia.DefaultObject](api:evennia.objects.objects#evennia.objects.objects.DefaultObject) - base class for all objects ([docs](Components/Objects))
- [evennia.DefaultCharacter](api:evennia.objects.objects#evennia.objects.objects.DefaultCharacter) - base class for in-game characters ([docs](Components/Objects#Character))
- [evennia.DefaultRoom](api:evennia.objects.objects#evennia.objects.objects.DefaultRoom) - base class for rooms ([docs](Components/Objects#Room))
- [evennia.DefaultExit](api:evennia.objects.objects#evennia.objects.objects.DefaultExit) - base class for exits ([docs](Components/Objects#Exit))
- [evennia.DefaultScript](api:evennia.scripts.scripts#evennia.scripts.scripts.DefaultScript) - base class for OOC-objects ([docs](Components/Scripts))
- [evennia.DefaultChannel](api:evennia.comms.comms#evennia.comms.comms.DefaultChannel) - base class for in-game channels ([docs](Components/Channels))

### Commands

- [evennia.Command](api:evennia.commands.command#evennia.commands.command.Command) - base [Command](Components/Commands) class. See also `evennia.default_cmds.MuxCommand`
- [evennia.CmdSet](api:evennia.commands.cmdset#evennia.commands.cmdset.CmdSet) - base [Cmdset](Components/Command-Sets) class
- [evennia.default_cmds](api:Default-Command-Help) - access all default command classes as properties

- [evennia.syscmdkeys](api:Commands#System-Commands) - access system command keys as properties

### Utilities

- [evennia.utils.utils](api:evennia.utils.utils) - mixed useful utilities
- [evennia.gametime](api:evennia.utils.gametime) - server run- and game time ([docs](Components/Coding-Utils#gametime))
- [evennia.logger](api:evennia.utils.logger) - logging tools
- [evennia.ansi](api:evennia.utils.ansi) - ansi coloring tools
- [evennia.spawn](api:evennia.prototypes.spawner#evennia.prototypes.spawner.Spawn) - spawn/prototype system ([docs](Components/Prototypes))
- [evennia.lockfuncs](api:evennia.locks.lockfuncs) - default lock functions for access control ([docs](Components/Locks))
- [evennia.EvMenu](api:evennia.utils.evmenu#evennia.utils.evmenu.EvMenu) - menu system ([docs](Components/EvMenu))
- [evennia.EvTable](api:evennia.utils.evtable#evennia.utils.evtable.EvTable) - text table creater
- [evennia.EvForm](api:evennia.utils.evform#evennia.utils.evform.EvForm) - text form creator
- Evennia.EvMore - text paginator
- [evennia.EvEditor](api:evennia.utils.eveditor#evennia.utils.eveditor.EvEditor) - in game text line editor ([docs](Components/EvEditor))
- [evennia.utils.funcparser.Funcparser](api:evennia.utils.funcparser) - inline parsing of functions ([docs](Components/FuncParser))

### Global singleton handlers

- [evennia.TICKER_HANDLER](api:evennia.scripts.tickerhandler) - allow objects subscribe to tickers ([docs](Components/TickerHandler))
- [evennia.MONITOR_HANDLER](api:evennia.scripts.monitorhandler) - monitor changes ([docs](Components/MonitorHandler))
- [evennia.CHANNEL_HANDLER](api:evennia.comms.channelhandler) - maintains channels
- [evennia.SESSION_HANDLER](api:evennia.server.serverhandler) - manages all sessionsmain session handler

### Database core models (for more advanced lookups)

- [evennia.ObjectDB](api:evennia.objects.models#evennia.objects.models.ObjectDB)
- [evennia.accountDB](api:evennia.accounts.models#evennia.accounts.models.AccountDB)
- [evennia.ScriptDB](api:evennia.scripts.models#evennia.scripts.models.ScriptDB)
- [evennia.ChannelDB](api:evennia.channels.models#evennia.channels.models.ChannelDB)
- [evennia.Msg](api:evennia.comms.models#evennia.comms.models.Msg)
- evennia.managers - contains shortcuts to all database managers

### Contributions

- [evennia.contrib](https://github.com/evennia/evennia/blob/master/evennia/contrib/) -
game-specific contributions and plugins ([docs](https://github.com/evennia/evennia/blob/master/evennia/contrib/README.md))
