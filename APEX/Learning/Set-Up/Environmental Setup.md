**1. Environment Specifications**

- Host OS: Arch Linux x86_64
- Emulator: QEMU ARM64
- Guest OS: Android 9 (API 28)
- Kernel version: 4.4.302-gcc24b0a8f68a
- Security patch level: 2019-08-05
- ADB connectivity: TCP 127.0.0.1:5555
- SELinux status: Permissive
- Root access: Confirmed

**2. Vulnerability Surface Confirmation**

- CVE-2019-2215 target function present: binder_proc_dec_tmpref
- Kernel symbol address: ffffff949777d1cc
- kptr_restrict: 0 (symbols readable)
- Patch status: Pre-December 2019, unpatched


**3. Screenshot:**

![[Pasted image 20261108031018.png]]