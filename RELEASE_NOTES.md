# Ultron v1.7.3

Ultron's name plate now projects through the real camera-owning overworld state instead of the public World API facade, which does not expose map scrolling.

The plate remains attached to Ultron's live sprite as he walks and as the camera scrolls around the map.

Ultron can also use eligible healing and status-recovery items during battle when they are present in his inventory. Items used by either generation's battle AI are consumed from that real inventory.

Supply runs now correctly leave interior rooms through their local staircase or doorway, including `LAST_MAP` return warps used by the player's bedroom, instead of walking in circles.
