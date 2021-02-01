**Engine Parts Durability** allows you to prevent engine parts from losing condition when a modular car is damaged.

## Recommended related plugins

- [Auto Engine Parts](https://umod.org/plugins/auto-engine-parts) -- Automatically fills engine modules with parts and prevents players from removing them
  - The functionality of Engine Parts Durability is included in Auto Engine Parts, so if you configure that plugin to apply to all cars (instead of just cars owned by players with permission), then Engine Parts Durability is redundant and can be uninstalled
- [No Engine Parts](https://umod.org/plugins/no-engine-parts) -- Allows car engines to work without engine parts

## Configuration

Default configuration:
```json
{
  "DurabilityLossMultiplier": 0.0
}
```

**By default, this plugin completely prevents damage to engine parts by using a multiplier of `0`.** The vanilla game uses `0.5`. This multiplier affects how much durability that engine parts (e.g., pistons, spark plugs) lose when a modular car is damaged. To customize, simply alter the `DurabilityLossMultiplier` configuration option and reload the plugin. This will immediately apply to engines on all existing cars, and to any engines that are added to cars while the plugin is loaded. Compatible with plugins that spawn cars with engines, unless they override the same multiplier.

## Uninstallation

To uninstall, set the multiplier to `0.5`, reload the plugin to apply the multiplier to all existing car engines, then unload/delete the plugin. Not necessary if you are wiping your server.

## Developer API

#### API_RefreshMultiplier

Plugins can call this API to refresh the durability loss multiplier for a particular `EngineStorage` container. This is useful if a plugin previously changed the internal damage multiplier and wants to reset it.

```csharp
void API_RefreshMultiplier(EngineStorage engineStorage)
```

## Developer Hooks

#### OnEngineDamageMultiplierChange

- Called when this plugin is about to change the internal damage multiplier of an engine storage container
- Returning `false` will prevent the damage multiplier from being changed
- Returning `null` will allow this plugin to change the damage multiplier

```csharp
object OnEngineDamageMultiplierChange(EngineStorage engineStorage, float desiredMultiplier)
```
