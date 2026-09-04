# Mori look mechanics

Mori is a humanoid 3D toy. The natural look motion starts in the eyes, then the eyelids and brows respond, followed by a small rigid head-and-neck turn. The shoulders and upper torso may follow by only a few pixels while the lower torso, hips, legs, and feet stay registered to the same baseline. Preserve the skull, facial spacing, hair shape, vest volume, and adult expression; do not warp the face or rotate the whole sprite.

The black utility pouch is anchored by a strap from the shoulder to the opposite hip. The strap stays attached and follows the torso continuously. The pouch may lag by a very small amount when the torso turns, but it must not flip sides, detach, change size, or become a new prop. Both hands remain empty.

## Cardinal pose families

- `000 up`: pupils and whole eye surfaces aim upward, upper eyelids open slightly, chin lifts, and the head pitches back a little. The top plane of the face and hair becomes more visible while the lower face shortens. Torso and pouch remain anchored.
- `090 screen-right`: pupils, nose tip, and face turn clearly toward the image's right edge. The rightward cheek/profile leads, the opposite side of the face and far ear become less visible, and the head/neck yaw right with a restrained shoulder follow. The strap and pouch keep their physical attachment.
- `180 down`: pupils and whole eye surfaces aim down, upper eyelids lower slightly, chin tucks, and the head pitches forward. More crown and fringe become visible while the eyes remain readable. The torso may lean forward slightly; feet and pouch stay registered.
- `270 screen-left`: pupils, nose tip, and face turn clearly toward the image's left edge. The leftward cheek/profile leads, the opposite side of the face and far ear become less visible, and the head/neck yaw left with a restrained shoulder follow. The strap and pouch keep their physical attachment.

## Motion budget

Each 22.5-degree step advances the eyes, eyelids, head yaw or pitch, and shoulder follow by a similar small visual amount. The feet, hip center, overall scale, and lower-body silhouette remain fixed. Adjacent poses must not jump, flip the strap, change hair length, change facial proportions, or move the pouch to the other side. `157.5 -> 180` and `337.5 -> 000` receive the same one-step movement as every other boundary.
