# Kardex Support Suite 0.4.39

Release date: 2026-08-14 13:03

## Summary
- Stops rotating isometric warehouse sprite assets in customer renders so machines and packing equipment sit on the correct visual axis.
- Removes front/rear marker circles from exported customer render images while keeping orientation controls in the editor.
- Resizes warehouse render assets so reception, office, goods-out, dispatch and forklift are more visible, while trolleys are smaller.
- Reduces packing-machine render scale to prevent it sitting awkwardly against nearby items.
- Uses larger planning footprints for reception, office, dispatch, goods-out and packing machines so the customer render better reflects real warehouse scale.
- Spaces external lorry docks further apart and exports closer 16:9 isometric views to reduce wasted white space.

## Verification
- Built Kardex Support Suite.
- Built Advanced Strategy module.
- Created suite update package and manifest.
- Generated and visually checked a customer warehouse render smoke test.
