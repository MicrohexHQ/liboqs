liboqs algorithm datasheet: `kem_sidh`
====================================================

Summary
-------

- **Name**: SIDH
- **Algorithm type**: key exchange
- **Note**: SIDH is as ephemeral key exchange algorithm related to the SIKE KEM (sike.org) submitted to NIST. It is NOT secure to use it with static keys.
- **Main cryptographic assumption**: (supersingular) isogeny walk problem
- **Submitters' website**: https://github.com/Microsoft/PQCrypto-SIDH
- **Added to liboqs by**: Christian Paquin

Parameter sets
--------------

| Parameter set   | Security model | Claimed NIST security level | Public key size (bytes) | Secret key size (bytes) | Ciphertext size (bytes) | Shared secret size (bytes) |
|-----------------|:--------------:|:---------------------------:|:-----------------------:|:-----------------------:|:-----------------------:|:--------------------------:|
| Sidh-p434       |     IND-CPA    |              1              |            330          |             28          |            330          |            110             |
| Sidh-p503       |     IND-CPA    |              2              |            378          |             32          |            378          |            126             |
| Sidh-p610       |     IND-CPA    |              3              |            462          |             38          |            462          |            154             |
| Sidh-p751       |     IND-CPA    |              5              |            564          |             48          |            564          |            188             |

Implementation
--------------

- **Source of implementation:** https://github.com/Microsoft/PQCrypto-SIDH
- **Implementation version:** v3.1 (https://github.com/microsoft/PQCrypto-SIDH/tree/5ca332aca646b4c5a1f25ca712083b95f0acaf27)
- **License:** MIT License
- **Language:** C
- **Constant-time:** Yes
- **Architectures supported in liboqs master branch**: x86, x64

Additional comments
-------------------

No KAT are available for SIDH.
