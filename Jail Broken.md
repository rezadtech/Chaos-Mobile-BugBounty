# iOS Security tips


## Secure BootChain
To jail broke the IPhone, signiture validation must be broken. Two kind of jail broke is available:
1. Tethered: not presistance.
2. Untethered: presistance.



![Alternate image text](https://raw.githubusercontent.com/trelis24/trelis24.github.io/master/img/2018-06-13-Pentesting-iOS-Introduction/boot.png)

Levels of boot
1. Boot ROM: it contains the Apple root certificate with the authentic public key. Its code is contained in the processor and it can’t be updated or changed. It verifies that the LLB is properly signed and it has not been tampered before loading.
    
 2. Low-level boot loader (LLB): This is the lowest level of code that can be updated. It also verifies the signatures of firmware of iBoot before loading it.
    
3. iBoot: It verifies the signature of the iOS kernel before starting the kernel. This secure boot chain also prevents any malware that can affect at the boot level.

4. Kernel: after all the steps have been verified, the kernel can initialize.
5. Applications

** Note: Disable updates to preven iOS to revert jailed state

## Jailbreak iOS tools:
- https://canijailbreak.com/
- https://pangu8.com/
- https://chimera-jailbreak.com/jailbreak/
## Tools for install IPA files in IPhone:
- http://www.cydiaimpactor.com/
- Cydia app store
- Sileo app store

Refrences:
- https://support.apple.com/fr-fr/guide/security/secac71d5623/web
- https://trelis24.github.io/2018/06/13/Pentesting-iOS-Introduction/
