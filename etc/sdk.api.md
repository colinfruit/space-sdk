## API Report File for "@space/sdk"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { Buckets } from '@textile/hub';
import { Identity } from '@textile/crypto';
import { UserAuth } from '@textile/hub';

// @public (undocumented)
export class DirEntryNotFoundError extends Error {
    constructor(filePath: string, bucket: string);
}

// @public (undocumented)
export interface IdentityStorage {
    // (undocumented)
    add: (identity: Identity) => Promise<void>;
    // (undocumented)
    list: () => Promise<Identity[]>;
    // (undocumented)
    remove: (key: string) => Promise<void>;
}

// @public (undocumented)
export interface SpaceUser {
    // (undocumented)
    identity: Identity;
    // Warning: (ae-forgotten-export) The symbol "TextileStorageAuth" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    storageAuth?: TextileStorageAuth;
    // (undocumented)
    token: string;
}

// @public (undocumented)
export class UnauthenticatedError extends Error {
    constructor();
}

// @public
export class Users {
    constructor(config: UsersConfig, storage?: IdentityStorage);
    // (undocumented)
    authenticate(identity: Identity): Promise<SpaceUser>;
    // (undocumented)
    createIdentity(): Promise<Identity>;
    // (undocumented)
    list(): SpaceUser[];
    // (undocumented)
    remove(publicKey: string): Promise<void>;
    // (undocumented)
    static withStorage(storage: IdentityStorage, config: UsersConfig, onError?: CallableFunction): Promise<Users>;
}

// @public (undocumented)
export interface UsersConfig {
    // (undocumented)
    endpoint: string;
}

// @public
export class UserStorage {
    // Warning: (ae-forgotten-export) The symbol "UserStorageConfig" needs to be exported by the entry point index.d.ts
    constructor(user: SpaceUser, config?: UserStorageConfig);
    // Warning: (ae-forgotten-export) The symbol "CreateFolderRequest" needs to be exported by the entry point index.d.ts
    createFolder(request: CreateFolderRequest): Promise<void>;
    // Warning: (ae-forgotten-export) The symbol "ListDirectoryRequest" needs to be exported by the entry point index.d.ts
    // Warning: (ae-forgotten-export) The symbol "ListDirectoryResponse" needs to be exported by the entry point index.d.ts
    listDirectory(request: ListDirectoryRequest): Promise<ListDirectoryResponse>;
    // Warning: (ae-forgotten-export) The symbol "OpenFileRequest" needs to be exported by the entry point index.d.ts
    // Warning: (ae-forgotten-export) The symbol "OpenFileResponse" needs to be exported by the entry point index.d.ts
    openFile(request: OpenFileRequest): Promise<OpenFileResponse>;
    }


// (No @packageDocumentation comment for this package)

```