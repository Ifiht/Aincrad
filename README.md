Aincrad
[![Discord](https://img.shields.io/discord/289587909051416579.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/papermc)
===========

# Aincrad 🛡️
This is the custom server code used in the Minecraft world of Iðavöllr.

**Changes from PaperMC**
- [ ] Edit max speeds so minecart > horse > ice boat (paddles only, sails should still be fast)
- [ ] Implement Giants AI
- [ ] Implement Villager Tasks (Armorer heals golems, Priest heals villagers)
- [ ] Implement [Smallships](https://github.com/talhanation/smallships/tree/main)
- [ ] Implement [Accessories](https://github.com/wisp-forest/accessories/)
- [X] Implement [Sparkly](https://github.com/SparklyPower/SparklyPaper) per-world ticking 

How To (Fork Developers)
------
### Getting Started (new machines)
1. Clone repo
2. `./gradlew applyPatches` from root

### Apply Changes (per-file)
1. Make changes (in paper-server/src/minecraft/java)
2. `./gradlew fixupSourcePatches`
3. `./gradlew rebuildPatches`

### Apply Changes (feature)
1. Make changes (in paper-server/src/minecraft/java)
2. `git add .` in the java subfolder
3. `git commit -m` with the patch message (it will become the patch filename)
4. `./gradlew rebuildPatches` from root

#### Add files for patching
find the file needed using "view source" or manually in the gradle cache, add the full classpath to `./build-data/dev-imports.txt`, run the Gradle task "applyPatches", and you should be able to find your new NMS file in the `./Paper-Server` dir.

#### VERY helpful guide to patching:
[PaperMC Contrib](https://github.com/PaperMC/Paper/blob/master/CONTRIBUTING.md)
