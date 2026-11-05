ThreeHeadsDragon (Paper 1.21.11)

BUILD (needs JDK 21 + Maven):
  mvn package
  -> target/ThreeHeadsDragon.jar  -> put it in your server's plugins folder, restart.

WHAT IT DOES
  Reads the dragon's real head (and neck) hit boxes every tick and puts one extra head model
  3 blocks to the left and one 3 blocks to the right of it, pointing the same way and tilting
  the same way. Each extra head has its own hit box; damage to it is taken off the dragon.

SETTINGS: plugins/ThreeHeadsDragon/config.yml, then /threeheads reload
  spacing, scale, y-offset, forward-offset, hitbox-size, flip-facing, only-players, damage-multiplier
  neck, neck-segments, neck-size, neck-converge, neck-y-offset, neck-model, neck-spikes, neck-material, spike-material

NECKS: each extra head gets a neck of segments that follows the real neck's curve toward the body.
  Install ThreeHeadsDragon-ResourcePack.zip (client resourcepacks folder, or as server pack).
  It has the dragon's neck box + 'scale' spine using the dragon texture, so texture packs apply.
  With neck-model: false plain blocks (neck-material) are used instead. Change neck-converge to 0 for an exact parallel copy.

NOT INCLUDED: the jaw does not open on the extra heads.
