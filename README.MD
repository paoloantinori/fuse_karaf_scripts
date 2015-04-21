A collection of Karaf script to add functionality to JBoss Fuse Platform
------------------------------------------------------------------------

#### To install:

```bash
# just source the raw version of the file

JBossFuse:karaf@root> idof jline
Command not found: idof

JBossFuse:karaf@root> source https://raw.githubusercontent.com/paoloantinori/fuse_karaf_scripts/master/idof.karaf
((list -s | grep $args | tac) split '[ [ ]]' | head -n 2 | tail -n 1 | tac) trim

JBossFuse:karaf@root> idof jline
255
```

### TOC:
- `byteman.karaf`: Enables Byteman packages in bootdelegation classloader via a fragment 
```
source https://raw.githubusercontent.com/paoloantinori/fuse_karaf_scripts/master/byteman.karaf
```

- `features-dump.karaf`: Prints the content of all the available features known to runtime
```
source https://github.com/paoloantinori/fuse_karaf_scripts/raw/master/features-dump.karaf
# sample usage
features-dump 
```

- `idof.karaf`: Return numerical id of a bundle given a Symbolic-Name
```
source https://github.com/paoloantinori/fuse_karaf_scripts/raw/master/idof.karaf
# sample usage
idof jline
```

- `import-resources.karaf`: Import filesystem resources into a Fabric Profile
```
source https://github.com/paoloantinori/fuse_karaf_scripts/raw/master/import-resources.karaf
# sample usage
import-resource "paolo" "1.0" "broker.xml" "/tmp/paolotest"
```

- `log-levels.karaf`: Prints the current level of all the known Loggers registered on the platform 
```
source https://github.com/paoloantinori/fuse_karaf_scripts/raw/master/log-levels.karaf
log-levels
```

- `profiles-dump.karaf`: Recursively prints the content of all Fabirc profiles 
```
source https://github.com/paoloantinori/fuse_karaf_scripts/raw/master/profiles-dump.karaf
profiles-dump
```
