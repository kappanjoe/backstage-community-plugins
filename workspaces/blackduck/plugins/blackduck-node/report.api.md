## API Report File for "@backstage-community/plugin-blackduck-node"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { Config } from '@backstage/config';
import { LoggerService } from '@backstage/backend-plugin-api';

// @public (undocumented)
export type BD_CREATE_PROJECT_API_RESPONSE = {
  status: Number;
  location?: String;
};

// @public (undocumented)
export type BD_PROJECT_DETAIL = {
  name: string;
  projectLevelAdjustments: string;
  cloneCategories: [];
  customSignatureEnabled: string;
  customSignatureDepth: string;
  deepLicenseDataEnabled: string;
  snippetAdjustmentApplied: string;
  licenseConflictsEnabled: string;
  projectGroup: string;
  createdAt: string;
  createdBy: string;
  createdByUser: string;
  updatedAt: string;
  updatedBy: string;
  updatedByUser: string;
  source: string;
  _meta: META;
};

// @public (undocumented)
export type BD_PROJECTS_API_RESPONSE = {
  totalCount: Number;
  items: BD_PROJECT_DETAIL[];
  appliedFilters: [];
  _meta: META;
};

// @public (undocumented)
export type BD_REST_API_RESPONSE = {
  totalCount: Number;
  items: [];
  appliedFilters: [];
  _meta: META;
};

// @public (undocumented)
export type BD_VERISON_DETAIL = {
  versionName: string;
  phase: string;
  distribution: string;
  license: [];
  createdAt: string;
  createdBy: string;
  createdByUser: string;
  settingUpdatedAt: string;
  settingUpdatedBy: string;
  settingUpdatedByUser: string;
  source: string;
  _meta: META;
};

// @public (undocumented)
export type BD_VERSIONS_API_RESPONSE = {
  totalCount: Number;
  items: BD_VERISON_DETAIL[];
  appliedFilters: [];
  _meta: META;
};

// @public
export class BlackDuckConfig {
  // (undocumented)
  static fromConfig(config: Config): BlackDuckConfig;
  // (undocumented)
  getHostConfigByName(name: string): BlackDuckHostConfig;
}

// @public (undocumented)
export interface BlackDuckHostConfig {
  // (undocumented)
  host: string;
  // (undocumented)
  name: string;
  // (undocumented)
  token: string;
}

// @public (undocumented)
export class BlackDuckRestApi {
  constructor(logger: LoggerService, host: string, token: string);
  // (undocumented)
  auth(): Promise<any>;
  // (undocumented)
  createProject(
    projectName: string,
    projectVersion?: string,
    versionPhase?: string,
    versionDistribution?: string,
  ): Promise<BD_CREATE_PROJECT_API_RESPONSE>;
  // (undocumented)
  getProjects(name: string): Promise<BD_REST_API_RESPONSE>;
  // (undocumented)
  getProjectVersionDetails(
    projectName: string,
    projectVersion: string,
  ): Promise<any>;
  // (undocumented)
  getProjectVersions(projectName: string): Promise<BD_VERSIONS_API_RESPONSE>;
  // (undocumented)
  getRiskProfile(projectName: string, projectVersion: string): Promise<any>;
  // (undocumented)
  getVersions(
    projectUrl: string,
    versionName?: string,
  ): Promise<BD_VERSIONS_API_RESPONSE>;
  // (undocumented)
  getVulnerableComponents(
    projectName: string,
    projectVersion: string,
  ): Promise<any>;
}

// @public (undocumented)
export type META = {
  allow: [];
  href: string;
  links: [];
};
```
