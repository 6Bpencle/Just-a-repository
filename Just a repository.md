---- Minecraft Crash Report ----

WARNING: coremods are present:
  DLFMLCorePlugin ([动态光源]DynamicLights-1.10.2.jar)
  AstralCore (【星辉魔法】astralsorcery-1.4.5.jar)
  CXLibraryCore (cxlibrary-1.10.2-1.2.2.jar)
  llibrary (【冰火】llibrary-1.7.7-1.10.2.jar)
  IceAndFireForgeLoading (【冰火】iceandfire-1.0.1.jar)
Contact their authors BEFORE contacting forge


// Would you like a cupcake?


Time: 7/21/18 3:59 PM
Description: Ticking entity


java.lang.IllegalArgumentException: bound must be positive
        at java.util.Random.nextInt(Unknown Source)
        at com.sosnitzka.taiga.traits.TraitSlaughtering.onMobDrops(TraitSlaughtering.java:31)
        at net.minecraftforge.fml.common.eventhandler.ASMEventHandler_158_TraitSlaughtering_onMobDrops_LivingDropsEvent.invoke(.dynamic)
        at net.minecraftforge.fml.common.eventhandler.ASMEventHandler.invoke(ASMEventHandler.java:90)
        at net.minecraftforge.fml.common.eventhandler.EventBus.post(EventBus.java:185)
        at net.minecraftforge.common.ForgeHooks.onLivingDrops(ForgeHooks.java:514)
        at net.minecraft.entity.EntityLivingBase.func_70645_a(EntityLivingBase.java:1085)
        at net.minecraft.entity.EntityLivingBase.func_70097_a(EntityLivingBase.java:970)
        at de.teamlapen.vampirism.entity.EntityVampirism.func_70097_a(EntityVampirism.java:91)
        at slimeknights.tconstruct.tools.melee.item.Rapier.dealHybridDamage(Rapier.java:89)
        at slimeknights.tconstruct.tools.ranged.item.Bolt.dealDamageRanged(Bolt.java:133)
        at slimeknights.tconstruct.library.utils.ToolHelper.attackEntity(ToolHelper.java:679)
        at slimeknights.tconstruct.library.utils.ToolHelper.attackEntity(ToolHelper.java:572)
        at slimeknights.tconstruct.library.entity.EntityProjectileBase.dealDamage(EntityProjectileBase.java:314)
        at slimeknights.tconstruct.library.entity.EntityProjectileBase.onHitEntity(EntityProjectileBase.java:241)
        at slimeknights.tconstruct.library.entity.EntityProjectileBase.updateInAir(EntityProjectileBase.java:436)
        at slimeknights.tconstruct.library.entity.EntityProjectileBase.func_70071_h_(EntityProjectileBase.java:363)
        at net.minecraft.world.World.func_72866_a(World.java:1967)
        at net.minecraft.world.WorldServer.func_72866_a(WorldServer.java:839)
        at net.minecraft.world.World.func_72870_g(World.java:1937)
        at net.minecraft.world.World.func_72939_s(World.java:1750)
        at net.minecraft.world.WorldServer.func_72939_s(WorldServer.java:620)
        at net.minecraft.server.MinecraftServer.func_71190_q(MinecraftServer.java:709)
        at net.minecraft.server.MinecraftServer.func_71217_p(MinecraftServer.java:613)
        at net.minecraft.server.integrated.IntegratedServer.func_71217_p(IntegratedServer.java:240)
        at net.minecraft.server.MinecraftServer.run(MinecraftServer.java:471)
        at java.lang.Thread.run(Unknown Source)




A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------


-- Head --
Thread: Server thread
Stacktrace:
        at java.util.Random.nextInt(Unknown Source)
        at com.sosnitzka.taiga.traits.TraitSlaughtering.onMobDrops(TraitSlaughtering.java:31)
        at net.minecraftforge.fml.common.eventhandler.ASMEventHandler_158_TraitSlaughtering_onMobDrops_LivingDropsEvent.invoke(.dynamic)
        at net.minecraftforge.fml.common.eventhandler.ASMEventHandler.invoke(ASMEventHandler.java:90)
        at net.minecraftforge.fml.common.eventhandler.EventBus.post(EventBus.java:185)
        at net.minecraftforge.common.ForgeHooks.onLivingDrops(ForgeHooks.java:514)
        at net.minecraft.entity.EntityLivingBase.func_70645_a(EntityLivingBase.java:1085)
        at net.minecraft.entity.EntityLivingBase.func_70097_a(EntityLivingBase.java:970)
        at de.teamlapen.vampirism.entity.EntityVampirism.func_70097_a(EntityVampirism.java:91)
        at slimeknights.tconstruct.tools.melee.item.Rapier.dealHybridDamage(Rapier.java:89)
        at slimeknights.tconstruct.tools.ranged.item.Bolt.dealDamageRanged(Bolt.java:133)
        at slimeknights.tconstruct.library.utils.ToolHelper.attackEntity(ToolHelper.java:679)
        at slimeknights.tconstruct.library.utils.ToolHelper.attackEntity(ToolHelper.java:572)
        at slimeknights.tconstruct.library.entity.EntityProjectileBase.dealDamage(EntityProjectileBase.java:314)
        at slimeknights.tconstruct.library.entity.EntityProjectileBase.onHitEntity(EntityProjectileBase.java:241)
        at slimeknights.tconstruct.library.entity.EntityProjectileBase.updateInAir(EntityProjectileBase.java:436)
        at slimeknights.tconstruct.library.entity.EntityProjectileBase.func_70071_h_(EntityProjectileBase.java:363)
        at net.minecraft.world.World.func_72866_a(World.java:1967)
        at net.minecraft.world.WorldServer.func_72866_a(WorldServer.java:839)
        at net.minecraft.world.World.func_72870_g(World.java:1937)


-- Entity being ticked --
Details:
        Entity Type: tconstruct.bolt (slimeknights.tconstruct.tools.common.entity.EntityBolt)
        Entity ID: 9511
        Entity Name: entity.tconstruct.bolt.name
        Entity's Exact location: -41.24, 73.62, 481.07
        Entity's Block location: World: (-42,73,481), Chunk: (at 6,4,1 in -3,30; contains blocks -48,0,480 to -33,255,495), Region: (-1,0; contains chunks -32,0 to -1,31, blocks -512,0,0 to -1,255,511)
        Entity's Momentum: -36.55, -2.73, 26.37
        Entity's Passengers: []
        Entity's Vehicle: ~~ERROR~~ NullPointerException: null
Stacktrace:
        at net.minecraft.world.World.func_72939_s(World.java:1750)
        at net.minecraft.world.WorldServer.func_72939_s(WorldServer.java:620)


-- Affected level --
Details:
        Level name: 新 宝 岛 ： 深 渊 国 度
        All players: 1 total; [EntityPlayerMP['Lok_i'/251, l='新 宝 岛 ： 深 渊 国 度', x=-41.24, y=72.00, z=481.07]]
        Chunk stats: ServerChunkCache: 476 Drop: 0
        Level seed: 9203948668793535012
        Level generator: ID 06 - BIOMESOP, ver 0. Features enabled: true
        Level generator options: {"landScheme":"vanilla","tempScheme":"medium_zones","rainScheme":"medium_zones","biomeSize":"medium","amplitude":1.0,"generateBopOre":true,"generateBopSoils":true,"generateBopTrees":true,"generateBopGrasses":true,"generateBopFoliage":true,"generateBopFlowers":true,"generateBopPlants":true,"generateBopWaterPlants":true,"generateBopMushrooms":true,"generateRockFormations":true,"generatePoisonIvy":true,"generateFlax":true,"generateBerryBushes":true,"generateThorns":true,"generateQuicksand":true,"generateLiquidPoison":true,"generateHotSprings":true,"generateNetherHives":true,"generateNetherPlants":true,"generateEndFeatures":true}
        Level spawn location: World: (108,64,239), Chunk: (at 12,4,15 in 6,14; contains blocks 96,0,224 to 111,255,239), Region: (0,0; contains chunks 0,0 to 31,31, blocks 0,0,0 to 511,255,511)
        Level time: 2784024 game time, 16293 day time
        Level dimension: 0
        Level storage version: 0x04ABD - Anvil
        Level weather: Rain time: 42948 (now: false), thunder time: 46028 (now: false)
        Level game mode: Game mode: creative (ID 1). Hardcore: false. Cheats: false
Stacktrace:
        at net.minecraft.server.MinecraftServer.func_71190_q(MinecraftServer.java:709)
        at net.minecraft.server.MinecraftServer.func_71217_p(MinecraftServer.java:613)
        at net.minecraft.server.integrated.IntegratedServer.func_71217_p(IntegratedServer.java:240)
        at net.minecraft.server.MinecraftServer.run(MinecraftServer.java:471)
        at java.lang.Thread.run(Unknown Source)


-- System Details --
Details:
        Minecraft Version: 1.10.2
        Operating System: Windows 10 (amd64) version 10.0
        Java Version: 1.8.0_171, Oracle Corporation
        Java VM Version: Java HotSpot(TM) 64-Bit Server VM (mixed mode), Oracle Corporation
        Memory: 8374117528 bytes (7986 MB) / 10093592576 bytes (9626 MB) up to 10737418240 bytes (10240 MB)
        JVM Flags: 6 total; -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump -XX:+UseG1GC -XX:-UseAdaptiveSizePolicy -XX:-OmitStackTraceInFastThrow -Xmn128m -Xmx10240m
        IntCache: cache: 0, tcache: 0, allocated: 4, tallocated: 105
        FML: MCP 9.32 Powered by Forge 12.18.3.2511 Optifine OptiFine_1.10.2_HD_U_C2 48 mods loaded, 48 mods active
        States: 'U' = Unloaded 'L' = Loaded 'C' = Constructed 'H' = Pre-initialized 'I' = Initialized 'J' = Post-initialized 'A' = Available 'D' = Disabled 'E' = Errored
        UCHIJAAAA        mcp{9.19} [Minecraft Coder Pack] (minecraft.jar) 
        UCHIJAAAA        FML{8.0.99.99} [Forge Mod Loader] (forge-1.10.2-12.18.3.2511.jar) 
        UCHIJAAAA        Forge{12.18.3.2511} [Minecraft Forge] (forge-1.10.2-12.18.3.2511.jar) 
        UCHIJAAAA        LunatriusCore{1.1.2.36} [LunatriusCore] ([Mod依赖]LunatriusCore-1.10.2-1.1.2.36-universal.jar) 
        UCHIJAAAA        Roguelike{1.5.4} [Roguelike Dungeons] ([冒险地牢]RoguelikeDungeons-1.10.2-1.5.4.jar) 
        UCHIJAAAA        DynamicLights{1.4.3} [Dynamic Lights] ([动态光源]DynamicLights-1.10.2.jar) 
        UCHIJAAAA        DynamicLights_onFire{1.0.7} [Dynamic Lights Burning Entity Module] ([动态光源]DynamicLights-1.10.2.jar) 
        UCHIJAAAA        DynamicLights_creepers{1.0.6} [Dynamic Lights Creeper Module] ([动态光源]DynamicLights-1.10.2.jar) 
        UCHIJAAAA        DynamicLights_dropItems{1.1.0} [Dynamic Lights EntityItem Module] ([动态光源]DynamicLights-1.10.2.jar) 
        UCHIJAAAA        DynamicLights_entityClasses{1.0.1} [Dynamic Lights Entity Light Module] ([动态光源]DynamicLights-1.10.2.jar) 
        UCHIJAAAA        DynamicLights_mobEquipment{1.1.0} [Dynamic Lights Mob Equipment Light Module] ([动态光源]DynamicLights-1.10.2.jar) 
        UCHIJAAAA        DynamicLights_flameArrows{1.0.1} [Dynamic Lights Fiery Arrows Light Module] ([动态光源]DynamicLights-1.10.2.jar) 
        UCHIJAAAA        DynamicLights_floodLights{1.0.3} [Dynamic Lights Flood Light] ([动态光源]DynamicLights-1.10.2.jar) 
        UCHIJAAAA        DynamicLights_otherPlayers{1.0.9} [Dynamic Lights OtherPlayers Light Module] ([动态光源]DynamicLights-1.10.2.jar) 
        UCHIJAAAA        DynamicLights_thePlayer{1.1.3} [Dynamic Lights Player Light Module] ([动态光源]DynamicLights-1.10.2.jar) 
        UCHIJAAAA        Waila{1.7.0} [Waila] ([方块信息显示]Waila-1.7.0-B3_1.9.4.jar) 
        UCHIJAAAA        cxlibrary{1.2.2} [CXLibrary] (cxlibrary-1.10.2-1.2.2.jar) 
        UCHIJAAAA        MoreFurnaces{1.8.2} [More Furnaces] ([更多熔炉]MoreFurnaces-1.10.2-1.8.2.jar) 
        UCHIJAAAA        InGameInfoXML{2.8.1.85} [InGame Info XML] ([游戏信息显示]InGameInfoXML-1.10.2-2.8.1.85-universal.jar) 
        UCHIJAAAA        BiomesOPlenty{5.0.0.2089} [Biomes O' Plenty] ([超多生物群系]BiomesOPlenty-1.10.2-5.0.0.2089-universal.jar) 
        UCHIJAAAA        VeinMiner{0.34.1_1.9-73be663} [Vein Miner] ([连锁挖矿]VeinMiner-0.34.1-1.9r571+73be663.jar) 
        UCHIJAAAA        VeinMinerModSupport{0.34.1_1.9-73be663} [Mod Support] ([连锁挖矿]VeinMiner-0.34.1-1.9r571+73be663.jar) 
        UCHIJAAAA        WailaHarvestability{1.1.7} [Waila Harvestability] ([采掘信息显示]WailaHarvestability-mc1.10-1.1.7.jar) 
        UCHIJAAAA        JEI{3.14.7.419} [Just Enough Items] (【JEI】_1.10.2-3.14.7.419.jar) 
        UCHIJAAAA        llibrary{1.7.7} [LLibrary] (【冰火】llibrary-1.7.7-1.10.2.jar) 
        UCHIJAAAA        iceandfire{1.0.1} [Ice and Fire] (【冰火】iceandfire-1.0.1.jar) 
        UCHIJAAAA        mantle{1.10.2-1.1.5.205} [Mantle] (【匠魂】Mantle-1.10.2-1.1.5.jar) 
        UCHIJAAAA        tconstruct{1.10.2-2.6.5.10} [Tinkers' Construct] (【匠魂】TConstruct-1.10.2-2.6.5.jar) 
        UCHIJAAAA        taiga{1.2.6} [Tinkers Alloying Addon] (【匠魂合金附加】taiga-1.10.2-1.2.6.jar) 
        UCHIJAAAA        tinkertoolleveling{1.10.2-1.0.1.DEV.f5def58} [Tinkers Tool Leveling] (【匠魂工具升级】TinkerToolLeveling-1.10.2-1.0.1.jar) 
        UCHIJAAAA        TinkersAddons{1.0.6} [Tinkers' Addons] (【匠魂拓展】Tinkers'+Addons-1.10.2-1.0.6.jar) 
        UCHIJAAAA        moartinkers{0.4.1} [Moar Tinkers] (【匠魂更多材料】moartinkers-0.4.1.jar) 
        UCHIJAAAA        guideapi{@VERSION@} [Guide-API] (【吸血鬼】Guide-API-1.10.2-2.0.3-46.jar) 
        UCHIJAAAA        vampirism{1.1.3} [Vampirism] (【吸血鬼】Vampirism-1.10.2-1.1.3.jar) 
        UCHIJAAAA        teamlapen-lib{1.1.3} [TeamLapen Library] (【吸血鬼】Vampirism-1.10.2-1.1.3.jar) 
        UCHIJAAAA        gravestone{1.5.13} [Gravestone Mod] (【墓碑】gravestone-1.5.13.jar) 
        UCHIJAAAA        quickhotbar{1.04} [Quick Hotbar] (【快捷工具栏】Quick-Hotbar-Mod-1.10.2.jar) 
        UCHIJAAAA        lootbags{2.2.2} [Loot Bags] (【战利品】LootBags-1.10.2-2.2.2.jar) 
        UCHIJAAAA        astralsorcery{1.4.5} [Astral Sorcery] (【星辉魔法】astralsorcery-1.4.5.jar) 
        UCHIJAAAA        movillages{1.5.2} [Mo' Villages] (【更多村庄】Mo+Villages-1.5.2.jar) 
        UCHIJAAAA        Baubles{1.3.13} [Baubles] (Baubles-1.10.2-1.3.13.jar) 
        UCHIJAAAA        Botania{r1.9-341} [Botania] (【植物魔法】Botania r1.9-341.jar) 
        UCHIJAAAA        abyssalcraft{1.9.4.10} [AbyssalCraft] (【深渊国度】AbyssalCraft-1.10.2-1.9.4.10.jar) 
        UCHIJAAAA        harvestcraft{1.10.2j} [Pam's HarvestCraft] (【潘马斯丰收工艺】Pams+HarvestCraft+1.10.2j.jar) 
        UCHIJAAAA        grimoireofgaia{1.5.3} [Grimoire of Gaia 3] (【盖亚】GrimoireOfGaia3-1.10.2-1.5.3.jar) 
        UCHIJAAAA        thaumcraft{6.0.BETA8} [Thaumcraft] (【神秘时代6】Thaumcraft-1.10.2-6.0.BETA8.jar) 
        UCHIJAAAA        expandablebackpack{1.1} [Expandable Backpacks] (【背包】expandableBackpacks1.1.8-1.10.2.jar) 
        UCHIJAAAA        helpfultweaks{1.6.0} [Helpful Tweaks] (【腐肉皮革】Helpful Tweaks 1.10.2.jar) 
        Loaded coremods (and transformers): 
DLFMLCorePlugin ([动态光源]DynamicLights-1.10.2.jar)
  atomicstryker.dynamiclights.common.DLTransformer
AstralCore (【星辉魔法】astralsorcery-1.4.5.jar)
  
CXLibraryCore (cxlibrary-1.10.2-1.2.2.jar)
  cubex2.cxlibrary.CoreModTransformer
llibrary (【冰火】llibrary-1.7.7-1.10.2.jar)
  net.ilexiconn.llibrary.server.core.plugin.LLibraryTransformer
  net.ilexiconn.llibrary.server.core.patcher.LLibraryRuntimePatcher
IceAndFireForgeLoading (【冰火】iceandfire-1.0.1.jar)
  com.github.alexthe666.iceandfire.access.IceAndFireTransformer
        GL info: ~~ERROR~~ RuntimeException: No OpenGL context found in the current thread.
        Pulsar/tconstruct loaded Pulses: 
                - TinkerCommons (Enabled/Forced)
                - TinkerWorld (Enabled/Not Forced)
                - TinkerTools (Enabled/Not Forced)
                - TinkerHarvestTools (Enabled/Forced)
                - TinkerMeleeWeapons (Enabled/Forced)
                - TinkerRangedWeapons (Enabled/Forced)
                - TinkerModifiers (Enabled/Forced)
                - TinkerSmeltery (Enabled/Not Forced)
                - TinkerGadgets (Enabled/Not Forced)
                - TinkerOredict (Enabled/Forced)
                - TinkerIntegration (Enabled/Forced)
                - TinkerFluids (Enabled/Forced)
                - TinkerMaterials (Enabled/Forced)
                - TinkerModelRegister (Enabled/Forced)
                - WailaIntegration (Enabled/Not Forced)


        Profiler Position: N/A (disabled)
        Player Count: 1 / 8; [EntityPlayerMP['Lok_i'/251, l='新 宝 岛 ： 深 渊 国 度', x=-41.24, y=72.00, z=481.07]]
        Type: Integrated Server (map_client.txt)
        Is Modded: Definitely; Client brand changed to 'fml,forge'
        OptiFine Version: OptiFine_1.10.2_HD_U_C2
        Render Distance Chunks: 7
        Mipmaps: 1
        Anisotropic Filtering: 4
        Antialiasing: 2
        Multitexture: true
        Shaders: null
        OpenGlVersion: 4.6.0 NVIDIA 398.36
        OpenGlRenderer: GeForce GTX 960M/PCIe/SSE2
        OpenGlVendor: NVIDIA Corporation

        CpuCount: 4
