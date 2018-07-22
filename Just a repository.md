---- Minecraft Crash Report ----

WARNING: coremods are present:
  AstralCore (astralsorcery-1.12.2-1.9.3.jar)
  AppleCore (AppleCore-mc1.12.2-3.1.0.jar)
  Inventory Tweaks Coremod (InventoryTweaks-1.63.jar)
  EnderCorePlugin (EnderCore-1.12.2-0.5.35.jar)
  CoreMod (Aroma1997Core-1.12.2-2.0.0.0.b131.jar)
  IELoadingPlugin (ImmersiveEngineering-core-0.12-83.jar)
  OTGCorePlugin (OTG-Core.jar)
  DynamicSurroundingsCore (DynamicSurroundings-1.12.2-3.4.9.14.jar)
  BetterFoliageLoader (BetterFoliage-MC1.12-2.1.10.jar)
Contact their authors BEFORE contacting forge

// You're mean.

Time: 7/22/18 7:43 AM
Description: Exception in server tick loop

java.util.ConcurrentModificationException
	at java.util.IdentityHashMap$IdentityHashMapIterator.nextIndex(Unknown Source)
	at java.util.IdentityHashMap$KeyIterator.next(Unknown Source)
	at aroma1997.tatw.ic2usesfe.block.ICSourceEventListener.tick(ICSourceEventListener.java:76)
	at net.minecraftforge.fml.common.eventhandler.ASMEventHandler_1408_ICSourceEventListener_tick_WorldTickEvent.invoke(.dynamic)
	at net.minecraftforge.fml.common.eventhandler.ASMEventHandler.invoke(ASMEventHandler.java:90)
	at net.minecraftforge.fml.common.eventhandler.EventBus.post(EventBus.java:182)
	at net.minecraftforge.fml.common.FMLCommonHandler.onPreWorldTick(FMLCommonHandler.java:286)
	at net.minecraft.server.MinecraftServer.func_71190_q(MinecraftServer.java:752)
	at net.minecraft.server.MinecraftServer.func_71217_p(MinecraftServer.java:668)
	at net.minecraft.server.integrated.IntegratedServer.func_71217_p(IntegratedServer.java:252)
	at net.minecraft.server.MinecraftServer.run(MinecraftServer.java:526)
	at java.lang.Thread.run(Unknown Source)


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- System Details --
Details:
	Minecraft Version: 1.12.2
	Operating System: Windows 10 (amd64) version 10.0
	Java Version: 1.8.0_171, Oracle Corporation
	Java VM Version: Java HotSpot(TM) 64-Bit Server VM (mixed mode), Oracle Corporation
	Memory: 1909906512 bytes (1821 MB) / 4294967296 bytes (4096 MB) up to 4294967296 bytes (4096 MB)
	JVM Flags: 11 total; -XX:+UnlockExperimentalVMOptions -XX:+UseG1GC -XX:G1NewSizePercent=20 -XX:G1ReservePercent=20 -XX:MaxGCPauseMillis=50 -XX:G1HeapRegionSize=16M -XX:-UseAdaptiveSizePolicy -XX:-OmitStackTraceInFastThrow -Xmn128m -Xmx4096m -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump
	IntCache: cache: 0, tcache: 0, allocated: 13, tallocated: 95
	FML: MCP 9.42 Powered by Forge 14.23.4.2739 Optifine OptiFine_1.12.2_HD_U_E2_pre 102 mods loaded, 102 mods active
	States: 'U' = Unloaded 'L' = Loaded 'C' = Constructed 'H' = Pre-initialized 'I' = Initialized 'J' = Post-initialized 'A' = Available 'D' = Disabled 'E' = Errored

	| State     | ID                                | Version                  | Source                                             | Signature                                |
	|:--------- |:--------------------------------- |:------------------------ |:-------------------------------------------------- |:---------------------------------------- |
	| UCHIJAAAA | minecraft                         | 1.12.2                   | minecraft.jar                                      | None                                     |
	| UCHIJAAAA | mcp                               | 9.42                     | minecraft.jar                                      | None                                     |
	| UCHIJAAAA | FML                               | 8.0.99.99                | forge-1.12.2-14.23.4.2739.jar                      | e3c3d50c7c986df74c645c0ac54639741c90a557 |
	| UCHIJAAAA | forge                             | 14.23.4.2739             | forge-1.12.2-14.23.4.2739.jar                      | e3c3d50c7c986df74c645c0ac54639741c90a557 |
	| UCHIJAAAA | otgcore                           | 1.12.2 - v7              | minecraft.jar                                      | None                                     |
	| UCHIJAAAA | actuallyadditions                 | 1.12.2-r137              | ActuallyAdditions-1.12.2-r137.jar                  | None                                     |
	| UCHIJAAAA | ic2                               | 2.8.92-ex112             | Industrialcraft-2-2.8.92-ex112.jar                 | de041f9f6187debbc77034a344134053277aa3b0 |
	| UCHIJAAAA | advanced_solar_panels             | 4.2.0                    | Advanced+Solar+Panels-4.2.0.jar                    | None                                     |
	| UCHIJAAAA | applecore                         | 3.1.0                    | AppleCore-mc1.12.2-3.1.0.jar                       | None                                     |
	| UCHIJAAAA | jei                               | 4.11.0.204               | jei_1.12.2-4.11.0.204.jar                          | None                                     |
	| UCHIJAAAA | appleskin                         | 1.0.9                    | AppleSkin-mc1.12-1.0.9.jar                         | None                                     |
	| UCHIJAAAA | aroma1997core                     | 2.0.0.0.b131             | Aroma1997Core-1.12.2-2.0.0.0.b131.jar              | dfbfe4c473253d8c5652417689848f650b2cbe32 |
	| UCHIJAAAA | aromabackup                       | 2.1.1.3.b89              | AromaBackup-1.12.2-2.1.1.3.b89.jar                 | dfbfe4c473253d8c5652417689848f650b2cbe32 |
	| UCHIJAAAA | aromabackuprecovery               | 2.1.1.3.b89              | AromaBackup-1.12.2-2.1.1.3.b89.jar                 | None                                     |
	| UCHIJAAAA | baubles                           | 1.5.2                    | Baubles-1.12-1.5.2.jar                             | None                                     |
	| UCHIJAAAA | astralsorcery                     | 1.9.3                    | astralsorcery-1.12.2-1.9.3.jar                     | a0f0b759d895c15ceb3e3bcb5f3c2db7c582edf0 |
	| UCHIJAAAA | betterbuilderswands               | 0.11.1                   | BetterBuildersWands-1.12-0.11.1.245+69d0d70.jar    | None                                     |
	| UCHIJAAAA | betterfoliage                     | 2.1.10                   | BetterFoliage-MC1.12-2.1.10.jar                    | None                                     |
	| UCHIJAAAA | openterraingenerator              | v6                       | OpenTerrainGenerator-1.12.2+-+v6.jar               | e9f7847a78c5342af5b0a9e04e5abc0b554d69e0 |
	| UCHIJAAAA | biomebundle                       | 5.1                      | Biome_Bundle-1.12.2-v6.1.jar                       | None                                     |
	| UCHIJAAAA | biomesoplenty                     | 7.0.1.2394               | BiomesOPlenty-1.12.2-7.0.1.2394-universal.jar      | None                                     |
	| UCHIJAAAA | botania                           | r1.10-352                | Botania r1.10-352.jar                              | None                                     |
	| UCHIJAAAA | endercore                         | 1.12.2-0.5.35            | EnderCore-1.12.2-0.5.35.jar                        | None                                     |
	| UCHIJAAAA | codechickenlib                    | 3.2.0.345                | CodeChickenLib-1.12.2-3.2.0.345-universal.jar      | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
	| UCHIJAAAA | redstoneflux                      | 2.0.2                    | RedstoneFlux-1.12-2.0.2.3-universal.jar            | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| UCHIJAAAA | cofhcore                          | 4.5.3                    | CoFHCore-1.12.2-4.5.3.20-universal.jar             | None                                     |
	| UCHIJAAAA | cofhworld                         | 1.2.0                    | CoFHWorld-1.12.2-1.2.0.5-universal.jar             | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| UCHIJAAAA | thermalfoundation                 | 2.5.0                    | ThermalFoundation-1.12.2-2.5.0.19-universal.jar    | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| UCHIJAAAA | thermalexpansion                  | 5.5.0                    | ThermalExpansion-1.12.2-5.5.0.29-universal.jar     | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| UCHIJAAAA | enderio                           | 5.0.29                   | EnderIO-1.12.2-5.0.29.jar                          | None                                     |
	| UCHIJAAAA | enderiointegrationtic             | 5.0.29                   | EnderIO-1.12.2-5.0.29.jar                          | None                                     |
	| UCHIJAAAA | mantle                            | 1.12-1.3.1.21            | Mantle-1.12-1.3.1.21.jar                           | None                                     |
	| UCHIJAAAA | tconstruct                        | 1.12.2-2.10.1.87         | TConstruct-1.12.2-2.10.1.87.jar                    | None                                     |
	| UCHIJAAAA | ceramics                          | 1.12-1.3.3b              | Ceramics-1.12-1.3.3b.jar                           | None                                     |
	| UCHIJAAAA | chameleon                         | 1.12-4.1.3               | Chameleon-1.12-4.1.3.jar                           | None                                     |
	| UCHIJAAAA | chesttransporter                  | 2.8.7                    | ChestTransporter-1.12-2.8.7.jar                    | None                                     |
	| UCHIJAAAA | compactsolars                     | 1.12.2-5.0.17.340        | CompactSolars-1.12.2-5.0.17.340-universal.jar      | None                                     |
	| UCHIJAAAA | controlling                       | 3.0.6                    | Controlling-3.0.6.jar                              | None                                     |
	| UCHIJAAAA | cookingforblockheads              | 6.3.17                   | CookingForBlockheads_1.12.1-6.3.17.jar             | None                                     |
	| UCHIJAAAA | cucumber                          | 1.0.3                    | Cucumber-1.12-1.0.3.jar                            | None                                     |
	| UCHIJAAAA | cyclicmagic                       | 1.15.16                  | Cyclic-1.12.2-1.15.16.jar                          | None                                     |
	| UCHIJAAAA | dsurround                         | 3.4.9.14                 | DynamicSurroundings-1.12.2-3.4.9.14.jar            | 7a2128d395ad96ceb9d9030fbd41d035b435753a |
	| UCHIJAAAA | presets                           | 3.4.9.14                 | DynamicSurroundings-1.12.2-3.4.9.14.jar            | None                                     |
	| UCHIJAAAA | enderiobase                       | 5.0.29                   | EnderIO-1.12.2-5.0.29.jar                          | None                                     |
	| UCHIJAAAA | enderioconduits                   | 5.0.29                   | EnderIO-1.12.2-5.0.29.jar                          | None                                     |
	| UCHIJAAAA | enderioconduitsappliedenergistics | 5.0.29                   | EnderIO-1.12.2-5.0.29.jar                          | None                                     |
	| UCHIJAAAA | enderioconduitsopencomputers      | 5.0.29                   | EnderIO-1.12.2-5.0.29.jar                          | None                                     |
	| UCHIJAAAA | enderioconduitsrefinedstorage     | 5.0.29                   | EnderIO-1.12.2-5.0.29.jar                          | None                                     |
	| UCHIJAAAA | enderiointegrationforestry        | 5.0.29                   | EnderIO-1.12.2-5.0.29.jar                          | None                                     |
	| UCHIJAAAA | enderiointegrationticlate         | 5.0.29                   | EnderIO-1.12.2-5.0.29.jar                          | None                                     |
	| UCHIJAAAA | enderiomachines                   | 5.0.29                   | EnderIO-1.12.2-5.0.29.jar                          | None                                     |
	| UCHIJAAAA | enderiopowertools                 | 5.0.29                   | EnderIO-1.12.2-5.0.29.jar                          | None                                     |
	| UCHIJAAAA | extrautils2                       | 1.0                      | extrautils2-1.12-1.7.2.jar                         | None                                     |
	| UCHIJAAAA | fbp                               | 2.4.0                    | FancyBlockParticles-1.12.x-2.4.0.jar               | None                                     |
	| UCHIJAAAA | fastleafdecay                     | v14                      | FastLeafDecay-v14.jar                              | None                                     |
	| UCHIJAAAA | foamfix                           | 0.9.9.1-1.12.2           | foamfix-0.9.9.1-1.12.2-law.jar                     | None                                     |
	| UCHIJAAAA | ftbl                              | 4.2.5                    | FTBLib-4.2.5.jar                                   | None                                     |
	| UCHIJAAAA | ftbu                              | 4.2.4                    | FTBUtilities-4.2.4.jar                             | None                                     |
	| UCHIJAAAA | hud                               | 1.3.9                    | hud-1.3.9-1.12.jar                                 | None                                     |
	| UCHIJAAAA | waila                             | 1.8.23                   | Hwyla-1.8.23-B38_1.12.jar                          | None                                     |
	| UCHIJAAAA | theoneprobe                       | 1.4.19                   | theoneprobe-1.12-1.4.19.jar                        | None                                     |
	| UCHIJAAAA | immersiveengineering              | 0.12-83                  | ImmersiveEngineering-0.12-83.jar                   | 4cb49fcde3b43048c9889e0a3d083225da926334 |
	| UCHIJAAAA | immersivecables                   | 1.3.1                    | ImmersiveCables-1.12.2-1.3.1.jar                   | None                                     |
	| UCHIJAAAA | immersivepetroleum                | 1.1.9                    | ImmersivePetroleum-1.12.2-1.1.9.jar                | None                                     |
	| UCHIJAAAA | immersivetech                     | 1.3.10                   | Immersivetech-1.12-1.3.10.jar                      | None                                     |
	| UCHIJAAAA | inventorytweaks                   | 1.63+release.109.220f184 | InventoryTweaks-1.63.jar                           | 55d2cd4f5f0961410bf7b91ef6c6bf00a766dcbe |
	| UCHIJAAAA | jehc                              | 1.3.1                    | jehc-1.12-1.3.1.jar                                | None                                     |
	| UCHIJAAAA | journeymap                        | 1.12.2-5.5.2             | Journeymap-1.12.2-5.5.2.jar                        | None                                     |
	| UCHIJAAAA | jeresources                       | 0.8.6.28                 | JustEnoughResources-1.12.2-0.8.6.28.jar            | None                                     |
	| UCHIJAAAA | kleeslabs                         | 5.3.2                    | KleeSlabs_1.12-5.3.2.jar                           | None                                     |
	| UCHIJAAAA | mcjtylib_ng                       | 3.0.2                    | mcjtylib-1.12-3.0.2.jar                            | None                                     |
	| UCHIJAAAA | mekanism                          | 1.12.2-9.4.13.349        | Mekanism-1.12.2-9.4.13.349.jar                     | None                                     |
	| UCHIJAAAA | mekanismgenerators                | 9.4.11                   | MekanismGenerators-1.12.2-9.4.13.349.jar           | None                                     |
	| UCHIJAAAA | mekanismtools                     | 9.4.11                   | MekanismTools-1.12.2-9.4.13.349.jar                | None                                     |
	| UCHIJAAAA | mousetweaks                       | 2.8                      | MouseTweaks-2.8-mc1.12.1.jar                       | None                                     |
	| UCHIJAAAA | mysticalagriculture               | 1.6.7                    | mysticalagriculture-1.12-1.6.7.jar                 | None                                     |
	| UCHIJAAAA | mysticalagradditions              | 1.2.7                    | mysticalagradditions-1.12-1.2.7.jar                | None                                     |
	| UCHIJAAAA | otgflatlands                      | 1.0                      | OTG-Flatlands-1.12.2-v4.jar                        | None                                     |
	| UCHIJAAAA | otgskylands                       | 1.0                      | OTG-Skylands-1.12.2-v5.jar                         | None                                     |
	| UCHIJAAAA | otgvoid                           | 1.0                      | OTG-Void-1.12.2-v4.jar                             | None                                     |
	| UCHIJAAAA | harvestcraft                      | 1.12.2b                  | Pam's HarvestCraft 1.12.2b - Re-Balance Update.jar | None                                     |
	| UCHIJAAAA | stellarapi                        | 1.12.2-0.4.2.9           | Stellar+API-1.12.2-0.4.2.9.jar                     | None                                     |
	| UCHIJAAAA | photoptics                        | 1.12.2-0.1.1.1           | Photoptics-1.12.2-0.1.1.1.jar                      | None                                     |
	| UCHIJAAAA | rangedpumps                       | 0.5                      | rangedpumps-0.5.jar                                | None                                     |
	| UCHIJAAAA | redstonearsenal                   | 2.5.1                    | RedstoneArsenal-1.12.2-2.5.1.13-universal.jar      | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| UCHIJAAAA | xreliquary                        | 1.12.2-1.3.4.728         | Reliquary-1.12.2-1.3.4.728.jar                     | None                                     |
	| UCHIJAAAA | rftools                           | 7.54                     | rftools-1.12-7.54.jar                              | None                                     |
	| UCHIJAAAA | rftoolscontrol                    | 1.9.1                    | rftoolsctrl-1.12-1.9.1.jar                         | None                                     |
	| UCHIJAAAA | spiceoflife                       | 1.3.11                   | SpiceOfLife-mc1.12-1.3.11.jar                      | None                                     |
	| UCHIJAAAA | stellarsky                        | 1.12.2-0.5.2.8           | Stellar+Sky-1.12.2-0.5.2.8.jar                     | None                                     |
	| UCHIJAAAA | storagedrawers                    | 1.12-5.2.5               | StorageDrawers-1.12.1-5.3.3.jar                    | None                                     |
	| UCHIJAAAA | stg                               | 1.12.2-1.2.3             | SwingThroughGrass-1.12.2-1.2.3.jar                 | None                                     |
	| UCHIJAAAA | taiga                             | 1.3.2                    | Taiga-1.12.2-1.3.2.jar                             | None                                     |
	| UCHIJAAAA | tatw                              | 1.0.1.2.b19              | Tatw-1.12.2-1.0.1.2.b19.jar                        | dfbfe4c473253d8c5652417689848f650b2cbe32 |
	| UCHIJAAAA | thermaldynamics                   | 2.5.1                    | ThermalDynamics-1.12.2-2.5.1.14-universal.jar      | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| UCHIJAAAA | tinkertoolleveling                | 1.12-1.0.3.DEV.56fac4f   | TinkerToolLeveling-1.12-1.0.3.jar                  | None                                     |
	| UCHIJAAAA | torcherino                        | 7.1                      | torcherino-7.1.jar                                 | None                                     |
	| UCHIJAAAA | twilightforest                    | 3.5.263                  | twilightforest-1.12.2-3.5.263-universal.jar        | None                                     |
	| UCHIJAAAA | veinminer                         | 0.38.1                   | VeinMiner-1.12-0.38.1.639+134fb1e.jar              | None                                     |
	| UCHIJAAAA | veinminermodsupport               | 0.38.1                   | VeinMiner-1.12-0.38.1.639+134fb1e.jar              | None                                     |
	| UCHIJAAAA | wanionlib                         | 1.12.2-1.4               | WanionLib-1.12.2-1.4.jar                           | None                                     |
	| UCHIJAAAA | unidict                           | 1.12.2-1.9b              | UniDict-1.12.2-1.9b.jar                            | None                                     |

	Loaded coremods (and transformers): 
AstralCore (astralsorcery-1.12.2-1.9.3.jar)
  
AppleCore (AppleCore-mc1.12.2-3.1.0.jar)
  squeek.applecore.asm.TransformerModuleHandler
Inventory Tweaks Coremod (InventoryTweaks-1.63.jar)
  invtweaks.forge.asm.ContainerTransformer
EnderCorePlugin (EnderCore-1.12.2-0.5.35.jar)
  com.enderio.core.common.transform.EnderCoreTransformer
  com.enderio.core.common.transform.SimpleMixinPatcher
CoreMod (Aroma1997Core-1.12.2-2.0.0.0.b131.jar)
  
IELoadingPlugin (ImmersiveEngineering-core-0.12-83.jar)
  blusunrize.immersiveengineering.common.asm.IEClassTransformer
OTGCorePlugin (OTG-Core.jar)
  com.pg85.otg.forge.asm.OTGClassTransformer
DynamicSurroundingsCore (DynamicSurroundings-1.12.2-3.4.9.14.jar)
  org.blockartistry.DynSurround.asm.Transformer
BetterFoliageLoader (BetterFoliage-MC1.12-2.1.10.jar)
  mods.betterfoliage.loader.BetterFoliageTransformer
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
		- wailaIntegration (Enabled/Not Forced)
		- theoneprobeIntegration (Enabled/Not Forced)

	Ender IO: Found the following problem(s) with your installation (That does NOT mean that Ender IO caused the crash or was involved in it in any way. We add this information to help finding common problems, not as an invitation to post any crash you encounter to Ender IO's issue tracker. Always check the stack trace above to see which mod is most likely failing.):
                  * Optifine is installed. This is NOT supported.
                 This may (look up the meaning of 'may' in the dictionary if you're not sure what it means) have caused the error. Try reproducing the crash WITHOUT this/these mod(s) before reporting it.

	!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
	!!!You are looking at the diagnostics information, not at the crash.       !!!
	!!!Scroll up until you see the line with '---- Minecraft Crash Report ----'!!!
	!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

	Profiler Position: N/A (disabled)
	Player Count: 1 / 8; [EntityPlayerMP['Myrddin'/476, l='Biome Bundle', x=396.00, y=68.00, z=-1769.00]]
	Type: Integrated Server (map_client.txt)
	Is Modded: Definitely; Client brand changed to 'fml,forge'
	OptiFine Version: OptiFine_1.12.2_HD_U_E2_pre
	OptiFine Build: 20180718-153703
	Render Distance Chunks: 16
	Mipmaps: 0
	Anisotropic Filtering: 1
	Antialiasing: 0
	Multitexture: false
	Shaders: null
	OpenGlVersion: 4.6.0 NVIDIA 398.36
	OpenGlRenderer: GeForce GTX 980 Ti/PCIe/SSE2
	OpenGlVendor: NVIDIA Corporation
	CpuCount: 8
