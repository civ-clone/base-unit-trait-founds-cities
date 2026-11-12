# base-unit-trait-founds-cities

The `FoundsCities` unit trait: a unit type with it can found a city, or join one.

A unit type with this trait can found a new city, or add itself to an existing one.

For example: Civ1 and Civ2: Settlers (Civ2: Engineers too).

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(FoundsCities)`:

```ts
import FoundsCities from '@civ-clone/base-unit-trait-founds-cities/FoundsCities';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, FoundsCities));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
