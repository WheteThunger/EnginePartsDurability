**Engine Parts Durability** allows you to alter the amount of durability that engine parts lose when a modular car is damaged.

## Configuration

```json
{
  "DurabilityLossMultiplier": 0.5
}
```

By default, this plugin uses the same durability loss multiplier as the vanilla game, `0.5`. This multiplier affects how much durability that engine parts (e.g., pistons, spark plugs) lose when a modular car is damaged. To customize, simply alter the `DurabilityLossMultiplier` configuration option and reload the plugin. This will immediately apply to engines on all existing cars, and to any engines that are added to cars while the plugin is loaded. Compatible with plugins that spawn cars with engines, unless they override the same multiplier.

 **To make engine parts take no damage, set `DurabilityLossMultiplier: 0`.**

## Uninstallation

This is an amazing plugin with basically no performance impact, so you obviously will never want to uninstall this, but if you do, simply set the multiplier back to `0.5`, reload the plugin to apply the multiplier to all existing car engines, then unload/delete the plugin. Not necessary if you are wiping your server.