A collection of Karaf script to add functionality to JBoss Fuse Platform
------------------------------------------------------------------------

#### To install:

```bash
# just source the raw version of the file

JBossFuse:karaf@root> idof jline
Command not found: idof

JBossFuse:karaf@root> source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/idof.karaf
((list -s | grep $args | tac) split '[ [ ]]' | head -n 2 | tail -n 1 | tac) trim

JBossFuse:karaf@root> idof jline
255
```

### TOC:
- `lang_utils.karaf`: Generic helper aliases for other scripts, sequences, counters, etc...
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/lang_utils.karaf
# sample usage
countdown 10
```

- `byteman.karaf`: Enables Byteman packages in bootdelegation classloader via a fragment 
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/byteman.karaf
```

- `encrypt.karaf`: Encrypt values to be used in xmlns:enc="http://karaf.apache.org/xmlns/jasypt/v1.0.0"
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/encrypt.karaf
```

- `features-dump.karaf`: Prints the content of all the available features known to runtime
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/features-dump.karaf
# sample usage
features-dump 
```

- `find-pid.karaf`: Search for a key in ConfigAdmin for specified Fabric container and tells you which profile includes it
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/find-pid.karaf
# sample usage
find-pid "org.ops4j.pax" "root" "1.0" 
```

- `get-version-profile-version.karaf`: Tells you Fabric default version
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/get-version-profile-version.karaf
# sample usage
default-version
```

- `groovy.karaf`: Installs Groovy shell as a command
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/groovy.karaf
# sample usage
install_groovy
groovy:me '3 * 3'
a = "var in karaf scope" ; groovy:me var_in_groovy "$a" "var_in_groovy * 3" # ex. showing forwarding of karaf vars to groovy context
```

- `idof.karaf`: Return numerical id of a bundle given a Symbolic-Name
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/idof.karaf
# sample usage
idof jline
```

- `import-resources.karaf` and `import-resources-6.2.karaf`: Import filesystem resources into a Fabric Profile
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/import-resources.karaf
# or
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/import-resources-6.2.karaf
# sample usage
import-resource "paolo" "1.0" "broker.xml" "/tmp/paolotest.xml"
```

- `log-levels.karaf`: Prints the current level of all the known Loggers registered on the platform 
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/log-levels.karaf
# sample usage
log-levels
```

- `log-entry.karaf`: Adds a log entry into configured log file.
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/log-entry.karaf
# sample usage
log-entry this will be added to logs
```

- `log-set-multi.karaf`: Set a log level to each logger containing keyword (ignore case) in its name.
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/log-set-multi.karaf
# sample usage
log-set-multi DEBUG jolokia curator
```

- `profiles-dump.karaf`: Recursively prints the content of all Fabirc profiles 
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/profiles-dump.karaf
# sample usage
profiles-dump
```

- `scr-deactivate-by-id.karaf`: Deactivate a single SCR component, passing id
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/scr-deactivate-by-id.karaf
# sample usage
scr-deactivate-by-id 64
```

- `symbolic-names.karaf`: Produces a list of only symbolic-names of installed bundles
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/symbolic-names.karaf
# sample usage
symbolic-names
```

- `startup-levels.karaf`: Produces a list of startup levels of all bundles
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/startup-levels.karaf
# sample usage
startup-levels
```

- `zk-enable-autopurge.karaf`: Enable autopurge functionality for ZK 
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/profiles-dump.karaf
# sample usage
# Needs to be manually invoked due to a timing issue with dynamic-import!!!
```

- `zk-identify-leader.karaf`: Prints ZK network map 
```bash
source http://cdn.rawgit.com/paoloantinori/fuse_karaf_scripts/master/zk-identify-leader.karaf
# sample usage
# zk-map
```
