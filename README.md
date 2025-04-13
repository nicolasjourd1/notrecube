# JGames
A collection of minigame plugins for Minecraft running on a single server.

## Using
To use the plugins, you'll need a Minecraft 1.21.4 Spigot server. Also, a database is required by JAPI. Games can be launched without setting up a database, but nothing is saved.

### From release
Download the latest released archive and put its content in the plugin directory of your server.

### From source
An `install.sh` script is provided: it creates jars, copies them to the binary directory, and in the server plugins 
directory if it exists.

Also, a `release.sh` script is provided: it creates a release archive (i.e., it runs `install.sh` and zips the binary 
directory).

Alternatively, each plugin can be compiled separately using Maven in its directory. Each jar is located in the `target` 
directory, alongside `src`.

## Contributing
The project requires **JDK 21** and **Maven**.
You can start developing with minimal configuration using VSCode with the "*Extension Pack for Java*" extension. 

The provided `add-plugin` script creates a new plugin with the provided name :
```
./add-plugin MyPlugin
```
### Connecting to the database
The database must be set up in JAPI's `config.yml` file (`plugins/JAPI/config.yml`). In the following format :
```yaml
db:
  user: "user"
  password: "password"
  url: "url" # e.g. jdbc:mysql://host.com:port/db_name
```
