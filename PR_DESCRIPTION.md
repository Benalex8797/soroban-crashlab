# feat: Create cross-run board custom widgets

Closes #486

## Summary

This PR implements the frontend Cross-Run Board Custom Widgets feature, allowing maintainers to build custom analytical dashboards tracking cross-run behavior statistics.

- Built configurable widget components capable of being saved, reloaded, and seamlessly reordered within the grid.
- Extracted business logic (metric aggregation across FuzzingRuns and reorder bounds validation) into `custom-widgets-utils.ts` to ensure independent testing.
- Overhauled `create-cross-run-board-custom-widgets-63.tsx` with explicit persistence state bounds: mock network loading skeletons, an interactive saving spinner during modifications, and robust visual error boundaries when mutations fail.
- Expanded grid item semantics with robust ARIA controls. Specifically resolved grid keyboard accessibility limits by exposing functional keyboard-operable "Move left / Move right" action nodes alongside native drag-and-drop mouse events.
- Validated core aggregation algorithms with comprehensive unit tests for valid edge distributions and incorrect boundary tracking attempts.

## Validation

Primary:
```bash
cd apps/web
npm run lint
npm run build
```

Secondary:
```bash
cd apps/web
npm run test
```

Observed result:
- Skeletons appropriately defer to stored layout bounds post network latency.
- Tests (including out-of-bounds array splices for widgets and math aggregation mapping tests) pass under the node script locally.
- Functionality is safely modularized away from other tracking elements.
