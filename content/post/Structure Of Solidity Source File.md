+++
title = 'Structure Of Solidity Source File'
date = 2024-01-04T16:26:24+05:30
tags = ['solidity', 'web3', 'smart contract']
+++

The layout of a Solidity source file typically includes several components:

1. SPDX License Identifier: It's recommended to start each file with a comment indicating the license under which the code is released. This is often done using SPDX license identifiers, making the license machine-readable.

    ```solidity
    // SPDX-License-Identifier: MIT
    ```

2. Pragmas: Pragmas are directives used to enable specific compiler features or checks. There are different types of pragmas, such as version pragma and ABI Coder pragma.

   a. Version Pragma: Specifies the Solidity compiler version to be used for compilation. It helps reject compilation with future incompatible versions.

   ```solidity
   pragma solidity ^0.5.2;
   ```

   b. ABI Coder Pragma: Selects between different implementations of the ABI encoder and decoder. For example, 
   
   ```solidity
   pragma abicoder v1 or pragma abicoder v2.
   ```

3. Importing other Source Files: Solidity supports import statements similar to JavaScript. They help modularize code by importing symbols from other files.

    ```solidity
    import "filename";
    import * as symbolName from "filename";
    import "filename" as symbolName;
    import {symbol1 as alias, symbol2} from "filename";
    ```

4. Comments: Single-line (//) and multi-line (/* ... */) comments are supported. NatSpec comments (/// or /** ... */) are also available for documentation purposes.

    ```solidity
    // This is a single-line comment.

    /*
    This is a
    multi-line comment.
    */
    ```

5. Contract: Contracts in solidity are similar to classess in object oriented languages, and these are the main part of our source file.
    ```solidity
    contract ContractName{
        //body of our smart contract
    }
    ```

These components collectively form the structure of a Solidity source file, facilitating readability, maintainability, and compliance with licensing and versioning requirements.