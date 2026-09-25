# Barber
Barber module for cmangos vanilla and tbc cores which will allow the players to change their look after creating their character.

The Barber npc will be located in Stormwind Trade District and in Orgrimmar <PlaceHolder>.

# Available Cores
Classic and TBC

# How to install
1. Follow the instructions in https://github.com/davidonete/cmangos-modules?tab=readme-ov-file#how-to-install
2. Enable the `BUILD_MODULE_BARBER` flag in cmake and run cmake. The module should be installed in `src/modules/barber`
3. Copy the configuration file from `src/modules/dualspec/src/barber.conf.dist.in` and place it where your mangosd executable is. Also rename it to `barber.conf`.
4. Remember to edit the config file and modify the options you want to use.
5. Lastly you will have to install the database changes located in the `src/modules/dualspec/sql/install` folder, each folder inside represents where you should execute the queries. E.g. The queries inside of `src/modules/barber/sql/install/world` will need to be executed in the world/mangosd database.

# How to uninstall
To remove the dual spec from your server you have multiple options, the first and easiest is to disable it from the `barber.conf` file. The second option is to completely remove it from the server and db:
1. Remove the `BUILD_MODULE_BARBER` flag from your cmake configuration and recompile the game
2. Execute the sql queries located in the `src/modules/barber/sql/uninstall` folder. Each folder inside represents where you should execute the queries. E.g. The queries inside of `src/modules/barber/sql/uninstall/world` will need to be executed in the world/mangosd database.
