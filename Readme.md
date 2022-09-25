# Randomness Test

POC of a randomness generator for artgobblers. This model ensures even if 9999 gobblers are minted, the last one's emissionMultiple will still be guaranteed to be random.

## Requirements

-   jupyter + python3.9+
-   numpy
-   matplotlib

## Details

This notebook generates a seed mimicing uint64 chainlinkVRF seed. It then does a random shuffle, and considers a random number of them to be pre-minted. Then instead of using swapIds to generate the pdf, it uses (swapId\*seed)%10000 to generate the pdf. This ensures that even the last gobbler's emissionMultiple will be random since it depends on the seed.
