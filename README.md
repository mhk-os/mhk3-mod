# mhk3-mod

Moorhuhn Kart 3 as a mod for Moorhuhn Kart: Open Source Edition, with 8 tracks, 3 drivers, karts, powerups and effects converted from the original game. The game ships it preinstalled and builds it from this repository. Every push to main also publishes a GitHub release with a zip per platform that you can put into the Mods folder of the game to install a newer build.

## Audio

Music (including menu/title/highscore cues) is normalized per song to -16 LUFS. Effects use one attenuation-only gain per source game, matching group medians to the quietest source while preserving intentional differences between cues; borrowed clips follow their source game's gain. Decoded peaks stay below 0 dBFS. Local cue gains and track music volumes are unchanged.

## Shrinker

The shrink ray reduces kart size and engine top speed to 27%, with half acceleration, for 10 seconds. A hit also reduces current horizontal velocity to 27% so a kart cannot coast at its old speed after shrinking; vertical velocity is preserved. Driving modifiers return to normal when the effect ends.

## Character portraits

Each driver's icon and portrait share the `mhk3.<character>_portrait.png` in its character directory. Replace the PNG in place and retain its `.meta` file to preserve references. Keep the matching PNG in the game's `Assets/MHK/UI/Samples/` directory in sync for menu previews.

## Track variants

Pirate Island, Robin Hood and UFO can be driven in reverse. Every track except UFO has a time of day option, Pirate Island is at night by default, and UFO always counts as night (headlights on). Shimalaya has snow, Egypt a sandstorm and the other tracks except UFO rain. The overlay definitions are in each track's `Variants` folder, the overlay scenes (`<track>.night.unity`, `<track>.day.unity`, `<track>.rain.unity`, `<track>.snow.unity`, `<track>.sandstorm.unity`, `<track>.reverse.unity`) next to the track scene, the cover map for rain (`<track>.cover.asset`) beside them and the generated night, day, rain, snow and sandstorm skies in `Textures/Sky`. Night overlays darken the sun and ambient light and turn the karts' headlights on; rain adds rain with thunder, wet uncovered ground and less grip outdoors; snow adds snowfall and a little less grip outdoors; a sandstorm adds thick dusty fog and blowing sand. Reverse overlays turn the speed pad arrows round.

## License

MIT. Game assets belong to their respective owners. If there is a problem with any of them, message me and I will remove it.
