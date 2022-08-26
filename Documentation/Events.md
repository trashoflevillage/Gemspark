# Events
Events are triggers that can be subscribed to by [processes](Processes.md) via the '@' character. Whenever a process is subscribed to an event, the process will run whenever the event's trigger occurs.
You can subscribe a process to an event by doing the following:

``pro ProcessName() @ EventKeyword {}``

Unfortunately, due to forces outside of Gemspark's controls, there are some events that are locked behind **ranks**, DiamondFire's method of monetization.
<br>
<br>
<br>
# List of Events
|Keyword |Trigger |Cancellable |Rank Required
--- | --- | --- | ---
|PlayerJoinEvent|Triggers when a player joins the plot.|False|Default
|PlayerLeaveEvent|Triggers when a player leaves the plot.|False|Default
|PlayerCommandEvent|Triggers when a player runs a plot command. Plot commands start with '@'.|False|Emperor
|PlayerRightCLickEvent|Triggers when a player right clicks.|True|Default
|PlayerLeftCLickEvent|Triggers when a player left clicks.|True|Default
|PlayerRightClickEntityEvent|Triggers when a player right clicks an entity.|True|Default
|PlayerRightClickPlayerEvent|Triggers when a player right clicks another player.|False|Default
|PlayerPlaceBlockEvent|Triggers when a player places a block.|True|Default
|PlayerBreakBlockEvent|Triggers when a player breaks a block.|True|Default
|PlayerSwapHandsEvent|Triggers when a player swaps the items in their main and off hands.|True|Default
|PlayerChangeSlotEvent|Triggers when a player changes their held slot.|True|Default
|PlayerWalkEvent|Triggers while a player is walking.|True|Default
|PlayerJumpEvent|Triggers when a player jumps.|True|Default
|PlayerSneakEvent|Triggers when a player sneaks.|True|Default
|PlayerUnsneakEvent|Triggers when a player unsneaks.|True|Default
|PlayerStartSprintEvent|Triggers when a player starts sprinting.|True|Default
|PlayerStopSprintEvent|Triggers when a player stops sprinting.|True|Default
|PlayerStartFlyEvent|Triggers when a player starts flying.|True|Default
|PlayerStopFlyEvent|Triggers when a player stop flying.|True|Default
|PlayerRiptideEvent|Triggers when a player throws a trident with the riptide enchantment.|False|Default
|PlayerDismountEvent|Triggers when a player dismounts another entity.|True|Default
|PlayerHorseJumpEvent|Triggers when a player causes a horse to jump|False|Default
|PlayerVehicleJumpEvent|Triggers when a player presses the jump button whilst riding another entity.|False|Default
|PlayerClickMenuSlotEvent|Triggers when a player clicks a slot in a plot menu.|Automatic|Emperor
|PlayerClickInventorySlotEvent|Triggers when a player clicks a slot inside of their own or a block's inventory.|True|Default
|PlayerPickUpItemEvent|Triggers when a player picks up an item.|True|Default
|PlayerDropItemEvent|Triggers when a player drops up an item.|True|Default
|PlayerConsumeItemEvent|Triggers when a player consumes an item.|True|Default
|PlayerBreakItemEvent|Triggers when a player breaks an item.|True|Default
|PlayerCloseInventoryEvent|Triggers when a player closes an inventory.|False|Emperor
|PlayerFishEvent|Triggers when a player fishes an entity, player, or nothing.|True|Default
|PlayerTakeDamageEvent|Triggers when a player takes damage.|True|Default
|PlayerDamagePlayerEvent|Triggers when a player damages another player.|True|Default
|PlayerDamageEntityEvent|Triggers when a player damages an entity.|True|Default
|EntityDamagePlayerEvent|Triggers when a entity damages a player.|True|Default
|PlayerHealEvent|Triggers when a player regains health from any source.|True|Default
|PlayerShootBowEvent|Triggers when a player shoots a bow.|True|Default
|PlayerShootProjectileEvent|Triggers when a shoots a projectile.|True|Default
|PlayerProjectileHitEvent|Triggers when a player's projectile hits a block, an entity, or another player.|False|Default
|ProjectileDamagePlayerEvent|Triggers when a projectile damages an player.|True|Default
|PlayerCloudImbueEvent|Triggers when a player is given a status effect via an effect cloud.|True|Default
|PlayerDeathEvent|Triggers when a player dies.|True|Default
|PlayerKillPlayerEvent|Triggers when a player kills another player.|True|Default
|PlayerKillMobEvent|Triggers when a player kills an mob.|True|Default
|MobKillPlayerEvent|Triggers when a mob kills a player.|True|Default
|PlayerRespawnEvent|Triggers when a player respawns.|False|Default
