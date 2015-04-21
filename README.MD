A collection of Karaf script to add functionality to JBoss Fuse Platform
------------------------------------------------------------------------

To install:

```bash
# just source the raw version of the file

JBossFuse:karaf@root> idof jline
Command not found: idof

JBossFuse:karaf@root> source https://raw.githubusercontent.com/paoloantinori/fuse_karaf_scripts/master/idof.karaf
((list -s | grep $args | tac) split '[ [ ]]' | head -n 2 | tail -n 1 | tac) trim

JBossFuse:karaf@root> idof jline
255
```