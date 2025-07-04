## API Report File for "@backstage-community/plugin-blackduck"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { BackstagePlugin } from '@backstage/core-plugin-api';
import { Entity } from '@backstage/catalog-model';
import { JSX as JSX_2 } from 'react/jsx-runtime';
import { RouteRef } from '@backstage/core-plugin-api';
import { TableColumn } from '@backstage/core-components';
import { TableFilter } from '@backstage/core-components';

// @public (undocumented)
export const BlackDuckAllVersionPage: ({
  columns,
  filters,
}: {
  columns?: TableColumn<{}>[] | undefined;
  filters?: TableFilter[] | undefined;
}) => JSX_2.Element;

// @public (undocumented)
export const BlackDuckPage: ({
  columns,
  filters,
}: {
  columns?: TableColumn<{}>[] | undefined;
  filters?: TableFilter[] | undefined;
}) => JSX_2.Element;

// @public (undocumented)
export const blackduckPlugin: BackstagePlugin<
  {
    root: RouteRef<undefined>;
  },
  {},
  {}
>;

// @public (undocumented)
export const isBlackDuckAvailable: (entity: Entity) => boolean;

// @public (undocumented)
export const RiskCard: () => JSX_2.Element;

// (No @packageDocumentation comment for this package)
```
