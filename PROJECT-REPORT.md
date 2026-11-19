# Production report

## Goal

Create a playable website game featuring a speaking character in a furnished room, with interactive makeup application and Aholo Lux3D as the core asset pipeline.

## Asset workflow

1. Defined prompts for the character, eight cosmetic objects/tools, vanity, and bag (12 assets including separate mascara components and brushes).
2. Generated GLB exports using Lux3D G1 with cartoon styling for the character and PBR product styling for cosmetics.
3. Inspected the assets and normalized their dimensions and orientations for the game.
4. Optimized embedded textures for browser delivery without changing mesh geometry.
5. Added a local runtime rig, replacement articulated hands/arms and legs to the generated upper-body character.
6. Built the room, navigation, wardrobe, lounge, makeup masks, guided challenge and lookbook.
7. Recorded an 85-second walkthrough of the real game with dialogue and a readable preview HUD.

## Integration issue resolved

International account verification and quotes initially failed locally with RESPONSE_INVALID. The response included nanosecond timestamps not accepted by the installed Python 3.9 timestamp parser. Normalizing fractional seconds to supported precision allowed validation to succeed while retaining the original response checks. Generation subsequently completed for all 12 approved models. Credentials and account records are not included in this repository.

## Iterations

An early video-only result did not satisfy the playable-game objective and exposed disconnected hand/product motion. The implementation was rebuilt into an explorable web game. Products now share the palm grip transform, original overlapping hand geometry was removed, and individual application contact points were reviewed in-browser. The room includes a bed, wardrobe, lounge, coffee table, lamps, plants, shelves, vanity and cosmetic props.

## Validation

Browser checks covered the full six-step challenge, destinations, wardrobe colors, the lookbook, mobile layout, touch movement and product contact. The gameplay MP4 was decoded, its audio track checked, and representative frames inspected. See TESTED.md for scope and limitations.
