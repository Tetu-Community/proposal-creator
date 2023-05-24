## Steps to create a new tetuBAL voting round:

### Create the snapshot vote

1. Edit constants in `createBal` script
2. Set `DEPLOYER_MNEMONIC` variable (will use default derivation path)
3. Run `./createBal -d` and check output
4. Run `./createBal` to create round


### Create the tetubal "epoch"

1. In the `tetubal-bribes` repsitory, run `scripts/createEpoch -p <snapshot proposal id> -r <round number> -d <deadline>`. For example `scripts/createEpoch -p 0x8bbcfa519547de8f5ea6e5f99b914683860a6bf6c736cd9c7b9b2aba1266b400 -r 20 -d 1684206000`. This will send a transaction on the Polygon blockchain from the account that you configured earlier.

### Update the tetu-community website:

1. In the `tetu-community` repository, update `src/lib/consts.ts` to reflect the new round. Push to the main branch, which will automatically deploy to vercel.
