# SELODEV Survival Starter

A small, finished forest survival loop you can press Play on, plus every free
SELODEV Lite system already sitting in the project. No coding required.

Night is coming. Pick up the forager's rake, gather firewood and mushrooms from
the clearing, carry them to the camp sign, and craft a chest to make camp.
Movement is the Controller system, the rake is an Equipment item, holding it
raises a Foraging stat so every gather brings back double, your bag is the
Inventory system, the chest is a Crafting recipe, and the supply count is a
Quest. That is seven Lite systems in one small game. All fourteen are in
`addons/`, wired through one event bus.

## Play it (Godot 4.5 or newer)

Open this folder in Godot and press **Play (F5)**.

- **Move:** arrow keys or WASD
- **Take the rake:** walk over it and it equips. Foraging (top right) jumps to 2.
- **Gather:** walk over the logs and mushrooms. With the rake, each one brings
  back double, so supplies fill twice as fast.
- **Craft:** walk to the camp sign carrying 3 firewood and the chest builds itself
- **Save and Load:** buttons at the top right

## Make it yours

- `content/quests.json` is the camp checklist. Change the counts, retitle it,
  or add another objective. No scripts.
- The gatherables are `game/survival/items/*.tres` resources: id, name, icon.
  Add a `berries.tres`, drop a pickup in the scene, add its id to the quest,
  and the counter tracks it.
- `game/survival/foraging_stat.tres` is the Foraging value each gather reads,
  and the rake's +1 is one line in `game/survival/survival_player.gd`. Raise the
  base or the bonus and gathering gets richer.
- The recipe lives on the camp sign: select `CampSpot` in the editor and change
  `wood_needed` in the Inspector.
- `game/art/kenney/` is the pixel art, CC0 from Kenney's Tiny Town and Tiny
  Dungeon packs (credits in `CREDITS.md`). Overwrite a PNG with your own and
  the game picks it up.
- The clearing is one rect on the `Ground` node. Resize it in the Inspector
  and the tree line, its collision and the camera all follow.
- Eleven more systems ship switched off. Turn one on in Project Settings then
  Plugins when your game wants it.

## Run the checks yourself

```bash
godot --headless --path . tools/survival/verify.tscn
```

Every other system carries its own suite under `tools/` as well.

## Growing out of the Lite tier

Each Lite system is the free cut of a paid one. The full versions of everything
in this project, plus the Game Kit that wires them together, ship in one
package: **SELODEV Complete** on https://selodev.com/go/complete. One purchase, every
system, drop-in upgrades. Your content and scenes keep working.

## License

MIT for the kit. The art is CC0, credited in `CREDITS.md`. Make it, rename it,
ship it, sell it. That's the point.


## Part of a family

This is one free tier from the selodev catalog of no-code Godot 4 systems. They share an item contract and a save contract, so they plug into each other, and each one also works fully on its own.

Free systems:

- [Inventory Lite](https://github.com/seloc0des/godot-inventory-lite)
- [Equipment Lite](https://github.com/seloc0des/godot-equipment-lite)
- [Loot Lite](https://github.com/seloc0des/godot-loot-lite)
- [Crafting Lite](https://github.com/seloc0des/godot-crafting-lite)
- [Vendor Lite](https://github.com/seloc0des/godot-vendor-lite)
- [Quests Lite](https://github.com/seloc0des/godot-quests-lite)
- [Stats / Skills Lite](https://github.com/seloc0des/godot-stats-skills-lite)
- [Save / Load Lite](https://github.com/seloc0des/godot-save-load-lite)
- [Dialogue Lite](https://github.com/seloc0des/godot-dialogue-lite)
- [Combat Lite](https://github.com/seloc0des/godot-combat-lite)
- [Controller Lite](https://github.com/seloc0des/godot-controller-lite)
- [Enemy AI Lite](https://github.com/seloc0des/godot-enemy-ai-lite)
- [Scene Flow Lite](https://github.com/seloc0des/godot-scene-flow-lite)
- [Audio Lite](https://github.com/seloc0des/godot-audio-lite)
- [Level Builder Lite](https://github.com/seloc0des/godot-level-builder-lite)
- [Weather System Lite](https://github.com/seloc0des/godot-weather-lite)
- [Settings + Menus](https://github.com/seloc0des/godot-settings-menus) (complete and free, no paid tier)

Free VFX: [Magic Cast](https://github.com/seloc0des/godot-magic-cast-vfx-lite), [Elemental Impact](https://github.com/seloc0des/godot-elemental-impact-vfx-lite), [Explosion](https://github.com/seloc0des/godot-explosion-vfx-lite), [Pickup, Buff & Heal](https://github.com/seloc0des/godot-pickup-buff-vfx-lite).

Free starter projects: [Free Starter](https://github.com/seloc0des/free-starter-godot), [Dungeon](https://github.com/seloc0des/godot-dungeon-starter), [Survival](https://github.com/seloc0des/godot-survival-starter), [RPG](https://github.com/seloc0des/godot-rpg-starter).

The full versions add drop-in UI, editor docks and the cross-system wiring. They're on itch.io: **https://selodev.itch.io**
