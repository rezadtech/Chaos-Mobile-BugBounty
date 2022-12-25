# iOS Security tips


## Secure BootChain
To jail broke the IPhone, signiture validation must be broken. Two kind of jail broke is available:
1. Tethered: not presistance.
2. Untethered: presistance.



![this is a test of how it works](https://help.apple.com/assets/627EBB4D4FDDD519030FB00A/627EBB504FDDD519030FB012/en_US/4624fc5cc6749103fdfcf21553ec313a.png)


![Alternate image text](https://raw.githubusercontent.com/trelis24/trelis24.github.io/master/img/2018-06-13-Pentesting-iOS-Introduction/boot.png)


    Boot ROM: it contains the Apple root certificate with the authentic public key. Its code is contained in the processor and it can’t be updated or changed. It verifies that the LLB is properly signed and it has not been tampered before loading.
    Low-level boot loader (LLB): This is the lowest level of code that can be updated. It also verifies the signatures of firmware of iBoot before loading it.
    iBoot: It verifies the signature of the iOS kernel before starting the kernel. This secure boot chain also prevents any malware that can affect at the boot level.
    Kernel: after all the steps have been verified, the kernel can initialize.


Refrences:
- https://support.apple.com/fr-fr/guide/security/secac71d5623/web
- https://trelis24.github.io/2018/06/13/Pentesting-iOS-Introduction/
