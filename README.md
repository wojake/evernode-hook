# Evernode Hook
Evernode utilizes [Hooks](https://hooks.xrpl.org/) on the XRPL to facilitate an open, permissionless and trustless layer-1 registry for [Evernode Hosts](https://github.com/HotPocketDev/evernode-host) and many more protocol-layer functionalities on Evernode. The Evernode Hook acts as the single point of truth that contains the relevent [parameters](https://github.com/HotPocketDev/evernode-hook/blob/main/src/constants.h) and data on the platform.

## Key Features of The Evernode Hook
- **Permissionless And Decentralized**: No single party controls the Evernode Hook, the Evernode Hook will be on top of a Blackholed XRPL account. Anyone, anywhere and at anytime can register on Evernode as a 3rd party host and start providing their hosting services on the platform.
- **On-chain Registry List**: Evernode Hosts must register on the Evernode Hook's registry list which represent their Registration on Evernode as a 3rd party hosting providers. The registry list will be maintained autonomously by the Evernode Hook and no single party controls it.
- **Hosting Rewards**: Registered Evernode Hosts are eligible to receive hosting rewards for every 1 Moment, if they are online and functioning.
- **Pruning Of Inactive Host**: The Hook will have the right to prune Evernode Hosts that are inactive for more than 240 Moments or 10 Days, this ensures Evernode stays reliable and active to the market. Pruned Evernode Hosts are still eligible to redeem 50% of their Registration Deposit whilst the other 50% goes to the reward pool for the current Epoch.

> NOTE: Evernode is still in a `work-in-progress` state: changes to the code, design, and structure may change as time progresses.

# Dev
Use `sudo apt-get install gcc-multilib` to install 32 bit gcc header files which is needed to compile hook as a 32 bit binary.

## Build
Run `make build` to build the hook binary and upload it to the hook account.

```bash
make build
```

Run `sethook.js` to upload the binary to the hook account.
```bash
node sethook.js
```

* Note: `make` will build and upload the binary at the same time.
* Note: `make upload` will create a hook.json file with default hook address and secret. This can be updated to change your hook account.
