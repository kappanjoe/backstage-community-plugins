## API Report File for "@backstage-community/plugin-mend-backend"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { BackendFeature } from '@backstage/backend-plugin-api';
import { ConditionalPolicyDecision } from '@backstage/plugin-permission-common';
import { Conditions } from '@backstage/plugin-permission-node';
import { PermissionCondition } from '@backstage/plugin-permission-common';
import { PermissionCriteria } from '@backstage/plugin-permission-common';
import { PermissionRule } from '@backstage/plugin-permission-node';
import { ResourcePermission } from '@backstage/plugin-permission-common';

// @public (undocumented)
export const createMendProjectConditionalDecision: (
  permission: ResourcePermission<RESOURCE_TYPE>,
  conditions: PermissionCriteria<PermissionCondition<RESOURCE_TYPE>>,
) => ConditionalPolicyDecision;

// @public (undocumented)
export type FilterProps = {
  ids: string[];
  exclude?: boolean;
};

// @public (undocumented)
export const mendConditions: Conditions<{
  filter: PermissionRule<
    {
      permission: {
        type: string;
        name: string;
        attributes: {
          action?: 'update' | 'read' | 'delete' | 'create' | undefined;
        };
        resourceType: RESOURCE_TYPE;
      };
      resourceRef: string;
    },
    FilterProps,
    RESOURCE_TYPE,
    {
      ids: string[];
      exclude?: boolean | undefined;
    }
  >;
}>;

// @public
const mendPlugin: BackendFeature;
export default mendPlugin;

// @public (undocumented)
export const mendReadPermission: ResourcePermission<RESOURCE_TYPE>;

// @public (undocumented)
export enum RESOURCE_TYPE {
  // (undocumented)
  PROJECT = 'mend-project',
}

// (No @packageDocumentation comment for this package)
```
