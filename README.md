**Engine Parts Durability** allows you to alter the amount of durability that engine parts lose when a modular car is damaged.

If you would rather your players not have to deal with engine parts, you can alternatively just use the [No Engine Parts](https://umod.org/plugins/no-engine-parts) plugin which allows car engines to work without engine parts.

## Configuration

Default configuration:
```json
{
  "DurabilityLossMultiplier": 0.0
}
```

**By default, this plugin completely disables damage to engine parts by using a multiplier of `0`.** The vanilla game uses `0.5`. This multiplier affects how much durability that engine parts (e.g., pistons, spark plugs) lose when a modular car is damaged. To customize, simply alter the `DurabilityLossMultiplier` configuration option and reload the plugin. This will immediately apply to engines on all existing cars, and to any engines that are added to cars while the plugin is loaded. Compatible with plugins that spawn cars with engines, unless they override the same multiplier.

## Uninstallation

To uninstall, set the multiplier to `0.5`, reload the plugin to apply the multiplier to all existing car engines, then unload/delete the plugin. Not necessary if you are wiping your server.
